---
title: Formuleontwerper in elektronische rapportage (ER)
description: In dit onderwerp wordt beschreven hoe de formuleontwerper in elektronische rapportage (ER) wordt gebruikt.
author: NickSelin
manager: AnnBe
ms.date: 05/14/2014
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 85d2370353520ee588dfe2aedf9998d707f0eda6
ms.sourcegitcommit: 97ed74889a09ef385f6ecbab69e84a05ff42ee41
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/20/2019
ms.locfileid: "1592655"
---
# <a name="formula-designer-in-electronic-reporting-er"></a>Formuleontwerper in elektronische rapportage (ER)

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe de formuleontwerper in elektronische rapportage (ER) wordt gebruikt. Wanneer u een indeling voor een specifiek elektronisch document in ER ontwerpt, kunt u formules gebruiken om gegevens te transformeren om te voldoen aan de vereisten voor de afhandeling en opmaak van het document. Deze formules lijken op formules in Microsoft Excel. Er worden diverse typen functies ondersteund in de formules: tekst, datum en tijd, wiskundige logica, informatie, gegevenstypeconversie en andere functies (functies specifiek voor het zakelijke domein).

## <a name="formula-designer-overview"></a>Overzicht van formuleontwerper

ER ondersteunt de Formuleontwerper. Daarom kunt u tijdens het ontwerpen expressies configureren die kunnen worden gebruikt voor de volgende taken in runtime:

- Het transformeren van gegevens die zijn ontvangen van een Microsoft Dynamics 365 for Finance and Operations-database en die moeten worden ingevoerd in een ER-gegevensmodel dat is ontworpen als een gegevensbron voor Emergency Recovery-indelingen. (Deze transformaties kunnen bijvoorbeeld filteren, groeperen en conversie van gegevenstype omvatten.)
- Gegevens opmaken die moet worden verzonden naar een genererend elektronisch document conform de indeling en de voorwaarden van een specifieke ER-indeling. (Bijvoorbeeld de opmaak kan worden uitgevoerd in overeenstemming met de aangevraagde taal of cultuur, of de codering.)
- Het proces van het maken van elektronische documenten beheren. (Bijvoorbeeld de expressies kunnen de uitvoer van specifieke elementen van de indeling inschakelen of uitschakelen, afhankelijk van de verwerking van gegevens. Ze kunnen ook het proces voor het maken van documenten onderbreken of berichten aan gebruikers tonen.)

U kunt de pagina **Formuleontwerper** openen wanneer u een van de volgende handelingen uitvoert:

- De binding van gegevensbronartikelen aan gegevensmodelonderdelen.
- De binding van gegevensbronartikelen aan indelingsonderdelen.
- Het onderhoud van berekende velden die deel uitmaken van gegevensbronnen.
- De definitie van zichtbaarheidvoorwaarden voor gebruikersinvoerparameters.
- Het ontwerp van transformaties van de indeling.
- De definitie van voorwaarden voor het inschakelen van de indelingsonderdelen.
- De definitie van bestandsnamen voor de bestandsonderdelen van de indeling.
- De definitie van de voorwaarden voor procescontrolevalidaties.
- De definitie van de berichttekst voor procescontrolevalidaties.

## <a name="designing-er-formulas"></a>ER-formules ontwerpen

### <a name="data-binding"></a>Gegevensbinding

De ER-formuleontwerper kan worden gebruikt om een expressie te definiëren voor de transformatie van gegevens die worden ontvangen van gegevensbronnen, zodat de gegevens tijdens runtime in de gegevensconsument kunnen worden ingevoerd:

- Vanuit Finance and Operations-gegevensbronnen en runtimeparameters naar een ER-gegevensmodel.
- Vanuit een ER-gegevensmodel naar een ER-indeling
- Vanuit Finance and Operations-gegevensbronnen en runtimeparameters naar een ER-indeling.

De volgende afbeelding toont het ontwerp van een expressie van dit type. In dit voorbeeld rondt de expressie de waarde van het veld **Intrastat.AmountMST** in de Intrastat-tabel in Finance and Operations af op twee decimalen en wordt de afgeronde waarde geretourneerd.

[![Gegevensbinding](./media/picture-expression-binding.jpg)](./media/picture-expression-binding.jpg)

De volgende afbeelding toont hoe een expressie van dit type kan worden gebruikt. In dit voorbeeld wordt het resultaat van de ontworpen expressie ingevoerd in het onderdeel **Transaction.InvoicedAmount** van het gegevensmodel **Belastingrapportagemodel**.

[![Gegevensbinding wordt gebruikt](./media/picture-expression-binding2.jpg)](./media/picture-expression-binding2.jpg)

Tijdens runtime rondt de ontworpen formule, **ROUND (Intrastat.AmountMST, 2)**, de waarde van het veld **AmountMST** voor elke record in de Intrastat-tabel af op twee decimalen. Vervolgens wordt de afgeronde waarde ingevoerd in het onderdeel **Transaction.InvoicedAmount** van het gegevensmodel **Btw-aangifte**.

### <a name="data-formatting"></a>Gegevensnotatie

De ER-formuleontwerper kan worden gebruikt om een expressie te definiëren voor de opmaak van gegevens die worden ontvangen van gegevensbronnen, zodat de gegevens kunnen worden verzonden als onderdeel van het genererende elektronische document. U hebt wellicht opmaak die moet worden toegepast als een normale regel die opnieuw moet worden gebruikt voor een indeling. U kunt in dit geval die opmaak één keer in de indelingsconfiguratie introduceren als een benoemde transformatie die een opmaakexpressie heeft. Deze benoemde transformatie kan vervolgens worden gekoppeld aan vele indelingscomponenten waarvan de uitvoer moet worden opgemaakt volgens de opmaakexpressie die u hebt gemaakt.

De volgende afbeelding toont het ontwerp van een transformatie van dit type. In dit voorbeeld kapt de transformatie **TrimmedString** inkomende gegevens van het gegevenstype **Tekenreeks** af door spaties vooraan en achteraan te verwijderen. Vervolgens wordt de afgekapte waarde geretourneerd.

[![Transformatie](./media/picture-transformation-design.jpg)](./media/picture-transformation-design.jpg)

De volgende afbeelding toont hoe een transformatie van dit type kan worden gebruikt. In dit voorbeeld wordt met verschillende opmaakonderdelen tijdens runtime tekst als uitvoer verzonden naar het genererende elektronische document. Alle opmaakonderdelen verwijzen bij naam naar de transformatie **TrimmedString**.

[![Transformatie wordt gebruikt](./media/picture-transformation-usage.jpg)](./media/picture-transformation-usage.jpg)

Wanneer indelingsonderdelen, zoals het onderdeel **partyName** in de vorige illustratie, verwijzen naar de transformatie **TrimmedString**, verzendt de transformatie tekst als uitvoer naar het genererende elektronische document. Deze tekst bevat geen spaties vooraan en achteraan.

Als u een opmaak hebt die afzonderlijk moet worden toegepast, kan deze opmaak als een afzonderlijke expressie van een binding van een specifieke indelingscomponent worden geïntroduceerd. De volgende afbeelding toont een expressie van dit type. In dit voorbeeld is het indelingsonderdeel **partyType** gebonden aan de gegevensbron via een expressie waarmee inkomende gegevens vanuit het veld **Model.Company.RegistrationType** in de gegevensbron worden geconverteerd naar tekst in hoofdletters. Vervolgens wordt die tekst als uitvoer verzonden naar het elektronische document.

[![Opmaak toepassen op een afzonderlijke component](./media/picture-binding-with-formula.jpg)](./media/picture-binding-with-formula.jpg)

### <a name="process-flow-control"></a>Processtroombeheer

De ER-formuleontwerper kan worden gebruikt om expressies te definiëren die de processtroom beheren voor het genereren van elektronische documenten. U kunt de volgende taken uitvoeren:

- Definieer voorwaarden die bepalen wanneer het maken van een document moet worden gestopt.
- Geef expressies op waarmee berichten voor gebruikers over gestopte processen of uitvoeringslogboekberichten over het voortzetten van het genereren van rapporten worden gemaakt.
- Geef de bestandsnamen op van genererende elektronische documenten en beheer de voorwaarden voor het maken hiervan.

Elke regel van het processtroombeheer is ontworpen als afzonderlijke validatie. De volgende afbeelding toont een validatie van dit type. Hier volgt een uitleg van de configuratie in dit voorbeeld:

- De validatie wordt geëvalueerd als het knooppunt **INSTAT** tijdens het genereren van het XML-bestand wordt gemaakt.
- Als de lijst met transacties leeg is, stopt de validatie het uitvoeringsproces en retourneert **FALSE**.
- De validatie retourneert een foutbericht dat de tekst van Finance and Operations-label SYS70894 bevat in de voorkeurstaal van de gebruiker.

[![Validatie](./media/picture-validation.jpg)](./media/picture-validation.jpg)

De ER-formuleontwerper kan ook worden gebruikt om een bestandsnaam te genereren voor een genererend elektronisch document en om een proces voor het maken van bestanden te beheren. De volgende afbeelding toont het ontwerp van een processtroombesturingselement van dit type. Hier volgt een uitleg van de configuratie in dit voorbeeld:

- De lijst met records uit de gegevensbron **model.Intrastat** is verdeeld in batches. Elke batch bevat maximaal 1000 records.
- De uitvoer maakt een zipbestand dat een bestand in XML-indeling bevat voor elke batch die is gemaakt.
- Een expressie retourneert een bestandsnaam voor genererende elektronische documenten door de bestandsnaam en bestandsextensie aaneen te schakelen. Voor de tweede en alle volgende batches bevat de bestandsnaam de batch-id als achtervoegsel.
- Een expressie activeert (door **TRUE** te retourneren) het maken van een bestand voor batches die ten minste één record bevatten.

[![Besturingselement voor bestanden](./media/picture-file-control.jpg)](./media/picture-file-control.jpg)

### <a name="basic-syntax"></a>Basissyntaxis

ER-expressies kunnen een of alle van de volgende elementen bevatten:

- Constanten
- Operatoren
- Verwijzingen
- Paden
- Functies

#### <a name="constants"></a>Constanten

Wanneer u expressies ontwerpt, kunt u tekst- en numerieke constanten (waarden die niet worden berekend) gebruiken. De expressie **VALUE ("100") + 20** gebruikt bijvoorbeeld de numerieke constante **20** en de tekenreeksconstante **"100"** en retourneert de numerieke waarde **120**. De ER-formuleontwerper ondersteunt escapereeksen. Daarom kunt u een expressiereeks opgeven die anders moet worden behandeld. De expressie **""Leo Tolstoy ""War and Peace"" Volume 1"** retourneert bijvoorbeeld de tekstreeks **Leo Tolstoy "War and Peace" Volume 1**.

#### <a name="operators"></a>Operatoren

De volgende tabel toont de rekenkundige operators die u kunt gebruiken om wiskundige basisbewerkingen uit te voeren, zoals optelling, aftrekking, deling en vermenigvuldiging.

| Operator | Betekenis               | Voorbeeld |
|----------|-----------------------|---------|
| +        | Optelling              | 1+2     |
| -        | Aftrekking, negatie | 5-2, -1 |
| \*       | Vermenigvuldigen        | 7\*8    |
| /        | Afdeling              | 9/3     |

De volgende tabel geeft de vergelijkingsoperatoren weer die worden ondersteund. U kunt deze operatoren gebruiken om twee waarden te vergelijken.

| Operator | Betekenis                  | Voorbeeld    |
|----------|--------------------------|------------|
| =        | Gelijk                    | X=Y        |
| &gt;     | Groter dan             | X&gt;Y     |
| &lt;     | Kleiner dan                | X&lt;Y     |
| &gt;=    | Groter dan of gelijk aan | X&gt;=Y    |
| &lt;=    | Kleiner dan of gelijk aan    | X&lt;=Y    |
| &lt;&gt; | Niet gelijk aan             | X&lt;&gt;Y |

Bovendien kunt u een ampersandteken (&) als tekstsamenvoegingsoperator gebruiken. Op deze manier kunt u twee tekstreeksen verbinden of samenvoegen tot één tekst.

| Operator | Betekenis     | Voorbeeld                                             |
|----------|-------------|-----------------------------------------------------|
| &        | Samenvoegen | "Er is niets om af te drukken" & ":&nbsp;" & "geen records gevonden" |

##### <a name="operator-precedence"></a>Operatorprioriteit

De volgorde waarin de onderdelen van een samenstellingsexpressie worden geëvalueerd, is belangrijk. Het resultaat van de expressie **1 + 4 / 2** verschilt bijvoorbeeld, afhankelijk van of de optellingsbewerking of de deelbewerking eerst wordt uitgevoerd. U kunt haakjes gebruiken om expliciet te definiëren hoe een expressie wordt geëvalueerd. Als u bijvoorbeeld wilt aangeven dat de optellingsbewerking eerst moet worden uitgevoerd, kunt u de voorafgaande expressie wijzigen in **(1 + 4) / 2**. Als u de volgorde van bewerkingen die moeten worden uitgevoerd in een expressie, niet expliciet aangeeft, wordt de volgorde gebaseerd op de standaardprioriteit die aan de ondersteunde operators is toegewezen. De volgende tabel toont de operators en de prioriteit die eraan is toegewezen. Operators met een hogere prioriteit (bijvoorbeeld 7) worden eerder geëvalueerd dan operators met een lagere prioriteit (bijvoorbeeld 1).

| Prioriteit | Operatoren      | Syntaxis                                                                  |
|------------|----------------|-------------------------------------------------------------------------|
| 7          | Groepering       | ( … )                                                                   |
| 6          | Toegankelijkheid voor leden  | … . …                                                                   |
| 5          | Functieaanroep  | … ( … )                                                                 |
| 4          | Vermenigvuldigen | … \* …<br>… / …                                                         |
| 3          | Additief       | … + …<br>… - …                                                          |
| 2          | Vergelijking     | … &lt; …<br>… &lt;= …<br>… =&gt; …<br>… &gt; …<br>… = …<br>… &lt;&gt; … |
| 1          | Scheidingsteken     | … , …                                                                   |

Als een expressie meerdere opeenvolgende operatoren met dezelfde prioriteit bevat, worden die bewerkingen van links naar rechts geëvalueerd. Bijvoorbeeld de expressie **1 + 6 / 2 \* 3 &gt; 5** retourneert **true**. We raden aan haakjes te gebruiken om de gewenste evaluatievolgorde van bewerkingen in expressies expliciet aan te geven, zodat de expressies gemakkelijker te lezen en onderhouden zijn.

#### <a name="references"></a>Verwijzingen

Alle gegevensbronnen van het huidige ER-onderdeel die tijdens het ontwerp van een expressie beschikbaar zijn, kunnen als benoemde verwijzingen worden gebruikt. (Het huidige ER-onderdeel kan een model of een indeling zijn.) Het huidige ER-gegevensmodel bevat bijvoorbeeld de gegevensbron **ReportingDate** en deze gegevensbron retourneert een waarde van het gegevenstype **DATETIME**. Om te zorgen dat deze waarde juist wordt opgemaakt in het genererende document kunt u als volgt verwijzen naar de gegevensbron in de expressie: **DATETIMEFORMAT (ReportingDate, "dd-MM-yyyy")**.

Alle tekens in de naam van een verwijzende gegevensbron die niet staan voor een letter van het alfabet, moeten worden voorafgegaan door een enkel aanhalingsteken ('). Als de naam van een verwijzende gegevensbron ten minste één symbool bevat dat geen letter van het alfabet voorstelt, moet de naam tussen enkele aanhalingstekens staan. (Deze niet-alfabetische symbolen kunnen bijvoorbeeld leestekens of andere geschreven symbolen zijn.) Hier volgen enkele voorbeelden:

- In een ER-expressie moet als volgt naar de gegevensbron **Datum en tijd van vandaag** worden verwezen: **'Datum en tijd van vandaag'**
- Naar de methode **name()** van de gegevensbron **Klanten** moet in een ER-expressie als volgt worden verwezen: **Customers.'name()'**

Als de methoden van Finance and Operations-gegevensbronnen parameters hebben, wordt de volgende syntaxis gebruikt om deze methoden aan te roepen:

- Naar de methode **isLanguageRTL** van de gegevensbron **Systeem** met een parameter **NL-NL** van het gegevenstype **Tekenreeks** moet in een ER-expressie als volgt worden verwezen: **System.'isLanguageRTL'("NL-NL")**.
- Aanhalingstekens zijn niet verplicht wanneer een methodenaam alleen alfanumerieke tekens bevat. Ze zijn wel verplicht voor een methode van een tabel als de naam haakjes bevat.

Als de gegevensbron **Systeem** wordt toegevoegd aan een ER-toewijzing die naar de Finance and Operations-toepassingsklasse **Global** verwijst, retourneert de expressie de Booleaanse waarde **FALSE**. De gewijzigde expressie **System ' isLanguageRTL'("AR")** retourneert de Booleaanse waarde **TRUE**.

U kunt de manier waarop waarden worden doorgegeven aan de parameters van dit type methode beperken:

- Alleen constanten kunnen worden doorgegeven aan methoden van dit type. De waarden van de constanten worden gedefinieerd in de ontwerpfase.
- Alleen primitieve (basis) gegevenstypen worden voor parameters van dit type ondersteund. (De primitieve gegevenstypen zijn geheel getal, real, Boolean, tekenreeks, enzovoort.)

#### <a name="paths"></a>Paden

Wanneer een expressie naar een gestructureerde gegevensbron verwijst, kunt u de paddefinitie gebruiken om een specifiek primitief element van deze gegevensbron te selecteren. Een puntteken (.) wordt gebruikt om afzonderlijke individuele elementen van een gestructureerde gegevensbron te scheiden. Het huidige ER-gegevensmodel bevat bijvoorbeeld de gegevensbron **InvoiceTransactions** die een lijst met records retourneert. De recordstructuur **InvoiceTransactions** bevat de velden **AmountDebit** en **AmountCredit**, die beide numerieke waarden retourneren. U kunt daarom de volgende expressie ontwerpen om het gefactureerde bedrag te berekenen: **InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit**.

#### <a name="functions"></a>Functies

Het volgende onderdeel beschrijft de taken die kunnen worden gebruikt in ER-expressies. Alle gegevensbronnen van de expressiecontext (het huidige ER-gegevensmodel of de huidige ER-indeling) en ook constanten kunnen als parameters worden gebruikt van functieaanroepen volgens de lijst met argumenten voor functieaanroepen. Constanten kunnen ook worden gebruikt als parameters van het aanroepen van functies. Het huidige ER-gegevensmodel bevat bijvoorbeeld de gegevensbron **InvoiceTransactions** die een lijst met records retourneert. De recordstructuur **InvoiceTransactions** bevat de velden **AmountDebit** en **AmountCredit**, die beide numerieke waarden retourneren. Voor het berekenen van het gefactureerde bedrag kunt u daarom de volgende expressie ontwerpen die de ingebouwde ER-afrondingsfunctie gebruikt: **ROUND (InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit, 2)**.

## <a name="supported-functions"></a>Ondersteunde functies

De volgende tabellen beschrijven de functies voor gegevensmanipulatie die u kunt gebruiken om ER-gegevensmodellen en ER-rapporten te ontwerpen. De lijst met functies is niet vast. Ontwikkelaars kunnen deze uitbreiden. Open het functievenster in de ER-formuleontwerper om de lijst van functies te bekijken die u kunt gebruiken.

### <a name="date-and-time-functions"></a>Datum- en tijdfuncties

| Functie | Beschrijving | Voorbeeld |
|----------|-------------|---------|
| ADDDAYS (datum/tijd, dagen) | Voeg het opgegeven aantal dagen aan de opgegeven datum-/tijdwaarde toe. | **ADDDAYS (NOW(), 7)** retourneert de datum en tijd van zeven dagen in de toekomst. |
| DATETODATETIME (datum) | Zet de opgegeven datumwaarde om naar een datum-/tijdwaarde. | **DATETODATETIME (CompInfo. 'getCurrentDate()')** retourneert de huidige Finance and Operations-sessiedatum, 24 december 2015, als **12/24/2015 12:00:00 AM**. In dit voorbeeld is **CompInfo** een ER-gegevensbron van het type **Finance and Operations/Table** waarmee naar de tabel CompanyInfo wordt verwezen. |
| NOW () | Retourneer de huidige datum en tijd van de Finance and Operations-toepassingsserver als een datum-/tijdwaarde. | |
| TODAY () | Retourneer de huidige datum van de Finance and Operations-toepassingsserver als een datumwaarde. | |
| NULLDATE () | Retourneer een **null**-datumwaarde. | |
| NULLDATETIME () | Retourneer een **null**-datum-/tijdwaarde. | |
| DATETIMEFORMAT (datum/tijd, indeling) | Converteer de opgegeven datum-/tijdwaarde naar een tekenreeks in de opgegeven indeling. (Zie voor informatie over de ondersteunde indelingen [standaard](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) en [aangepast](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx).) | **DATETIMEFORMAT (NOW(), "dd-MM.-yyyy")** retourneert de datum van de huidige Finance and Operations-toepassingsserver 24 december 2015 als **"24-12-2015"**, op basis van de opgegeven aangepaste notatie. |
| DATETIMEFORMAT (datum/tijd, indeling, cultuur) | Converteer de opgegeven datum-/tijdwaarde naar een tekenreeks in de opgegeven indeling en [cultuur](https://msdn.microsoft.com/en-us/goglobal/bb896001.aspx). (Zie voor informatie over de ondersteunde indelingen [standaard](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) en [aangepast](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx).) | **DATETIMEFORMAT (NOW(), "d", "de")** retourneert de huidige datum van de Finance and Operations-toepassingsserver 24 december 2015 als **"24.12.2015"**, op basis van de geselecteerde Duitse cultuur. |
| SESSIONTODAY () | Retourneer de huidige sessiedatum van de Finance and Operations-toepassingsserver als een datumwaarde. | |
| SESSIONNOW () | Retourneer de huidige sessiedatum en tijd van de Finance and Operations-toepassingsserver als een datum-/tijdwaarde. | |
| DATEFORMAT (datum, indeling) | Retourneer een tekenreeksvoorstelling van de opgegeven datum in de opgegeven indeling. | **DATEFORMAT (SESSIONTODAY (), "dd-MM-yyyy")** retourneert de huidige sessiedatum van Finance and Operations, 24 december 2015, als **"24-12-2015"**, op basis van de opgegeven aangepaste notatie. |
| DATEFORMAT (datum, indeling, cultuur) | Converteer de opgegeven datumwaarde naar een tekenreeks in de opgegeven indeling en [cultuur](https://msdn.microsoft.com/en-us/goglobal/bb896001.aspx). (Zie voor informatie over de ondersteunde indelingen [standaard](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) en [aangepast](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx).) | **DATETIMEFORMAT (SESSIONNOW (), "d", "de")** retourneert de huidige sessiedatum van Finance and Operations, 24 december 2015, als **"24.12.2015"**, op basis van de geselecteerde Duitse cultuur. |
| DAYOFYEAR (datum) | Retourneert de geheel-getalweergave van het aantal dagen tussen 1 januari en de opgegeven datum. | **DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))** retourneert **61**. **DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))** retourneert **1**. |
| DAYS (datum 1, datum 2) | Retourneert het aantal dagen tussen de opgegeven begindatum en de tweede opgegeven datum. Een positieve waarde als resultaat geven wanneer de eerste datum later is dan de tweede datum, **0** (nul) retourneren als de eerste datum gelijk is aan de tweede datum of een negatieve waarde retourneren als de eerste datum vroeger is dan de tweede datum. | **DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS(NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))** retourneert **-1**. |

### <a name="data-conversion-functions"></a>Functies voor gegevensconversie

| Functie | Omschrijving | Voorbeeld |
|----------|-------------|---------|
| DATETODATETIME (datum) | Zet de opgegeven datumwaarde om naar een datum-/tijdwaarde. | **DATETODATETIME (CompInfo. 'getCurrentDate()')** retourneert de huidige Finance and Operations-sessiedatum, 24 december 2015, als **12/24/2015 12:00:00 AM**. In dit voorbeeld is **CompInfo** een ER-gegevensbron van het type **Finance and Operations/Table** waarmee naar de tabel CompanyInfo wordt verwezen. |
| DATEVALUE (tekenreeks, notatie) | Retourneer een datumvoorstelling van de opgegeven tekenreeks in de opgegeven indeling. | **DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")** retourneert de datum 21 december 2016 volgens de opgegeven aangepaste notatie en de cultuur **EN-US** van de standaardtoepassing. |
| DATEVALUE (tekenreeks, notatie, cultuur) | Retourneer een datumvoorstelling van de opgegeven tekenreeks in de opgegeven indeling en cultuur. | **DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")** retourneert de datum 21 januari 2016, gebaseerd op de opgegeven aangepaste indeling en cultuur. Echter, **DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")** leidt tot een uitzondering en informeert de gebruiker dat de opgegeven tekenreeks niet als een geldige datum wordt herkend. |
| DATETIMEVALUE (tekenreeks, notatie) | Retourneer een datum/tijd-voorstelling van de opgegeven tekenreeks in de opgegeven indeling. | **DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")** retourneert 2:55:00 AM op 21 december 2016 op basis van de opgegeven aangepaste indeling en de cultuur **EN-US** van de standaardtoepassing. |
| DATETIMEVALUE (tekenreeks, notatie, cultuur) | Retourneer een datum/tijd-voorstelling van de opgegeven tekenreeks in de opgegeven indeling en cultuur. | **DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")** retourneert 2:55:00 AM op 21 december 2016 op basis van de opgegeven aangepaste indeling en cultuur. Echter, **DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy uu:mm:ss", "EN-US")** leidt tot een uitzondering en informeert de gebruiker dat de opgegeven tekenreeks niet als een geldige datum/tijd wordt herkend. |

### <a name="list-functions"></a>Lijstfuncties

<table>
<thead>
<tr>
<th>Functie</th>
<th>Omschrijving</th>
<th>Voorbeeld</th>
</tr>
</thead>
<tbody>
<tr>
<td>SPLIT (invoer, lengte)</td>
<td>Splits de opgegeven invoertekenreeks in subreeksen, waarvan elk de opgegeven lengte heeft. Retourneer het resultaat als een nieuwe lijst.</td>
<td><strong>SPLIT (&quot;abcd&quot;, 3)</strong> retourneert een nieuwe lijst die bestaat uit twee records die een <strong>STRING</strong>-veld hebben. Het veld in de eerste record bevat de tekst <strong>&quot;abc&quot;</strong> en het veld in de tweede record bevat de tekst <strong>&quot;d&quot;</strong>.</td>
</tr>
<tr>
<td>SPLIT (invoer, scheidingsteken)</td>
<td>Splits de opgegeven invoertekenreeks in subreeksen, op basis van het opgegeven scheidingsteken.</td>
<td><strong>SPLIT (&quot;XAb aBy&quot;, &quot;aB&quot;)</strong> retourneert een nieuwe lijst die bestaat uit drie records die een <strong>TEKENREEKS</strong>-veld hebben. Het veld in de eerste record bevat de tekst <strong>&quot;X&quot;</strong>, het veld in de tweede record bevat de tekst &quot;&nbsp;&quot; en het veld in de derde record bevat de tekst <strong>&quot;y&quot;</strong>. Als het scheidingsteken leeg is, wordt een nieuwe lijst geretourneerd die bestaat uit één record met een <strong>TEKENREEKS</strong>-veld dat de ingevoerde tekst bevat. Als de invoer leeg is, wordt een nieuwe lege lijst geretourneerd.
Als de invoer of het scheidingsteken niet is opgegeven (null), treedt een toepassingsuitzondering op.</td>
</tr>
<tr>
<td>SPLITLIST (lijst, aantal)</td>
<td>Splits de opgegeven lijst in batches waarvan elk het opgegeven aantal records bevat. Retourneer het resultaat als een nieuwe lijst batches die de volgende elementen bevatten:
<ul>
<li>Batches als normale lijsten (onderdeel <strong>Waarde</strong>)</li>
<li>Het huidige batchaantal (onderdeel <strong>BatchNumber</strong>)</li>
</ul>
</td>
<td>In het volgende voorbeeld wordt een gegevensbron <strong>Regels</strong> gemaakt als een recordlijst van drie records. Deze lijst is onderverdeeld in batches, die elk maximaal twee records bevatten.
<p><a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a></p>
<p>In de volgende afbeelding ziet u de ontworpen indelingslay-out. In deze indelingslay-out worden bindingen met de gegevensbron <strong>Regels</strong> gemaakt voor het genereren van uitvoer in XML-indeling. Deze uitvoer presenteert afzonderlijke knooppunten voor elke batch en de records daarin.</p>
<p><a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a></p>
<p>In de volgende afbeelding ziet u het resultaat wanneer de ontworpen indeling wordt uitgevoerd.</p>
<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>
</td>
</tr>
<tr>
<td>LIST (record 1 [, record 2, ...])</td>
<td>Retourneer een nieuwe lijst die wordt gemaakt van de opgegeven argumenten.</td>
<td><strong>LIST (model.MainData, model.OtherData)</strong> retourneert een lege record, waarbij de lijst met velden alle velden bevat van de recordlijsten <strong>MainData</strong> en <strong>OtherData</strong>.</td>
</tr>
<tr>
<td>LISTJOIN (lijst 1, lijst 2, ...)</td>
<td>Retourneer een gecombineerde lijst die wordt gemaakt van lijsten van opgegeven argumenten.</td>
<td><strong>LISTJOIN (SPLIT (&quot;abc&quot;, 1), SPLIT (&quot;def&quot;, 1))</strong> retourneert een lijst met zes records, waarbij één veld van het gegevenstype <strong>STRING</strong> enkele letters bevat.</td>
</tr>
<tr>
<td>ISEMPTY (lijst)</td>
<td>Retourneer <strong>TRUE</strong> als de opgegeven lijst geen elementen bevat. Retourneer anders <strong>FALSE</strong>.</td>
<td></td>
</tr>
<tr>
<td>EMPTYLIST (lijst)</td>
<td>Retourneer een lege lijst door de opgegeven lijst te gebruiken als een bron voor de lijststructuur.</td>
<td><strong>EMPTYLIST (SPLIT (&quot;abc&quot;, 1))</strong> retourneert een nieuwe lege lijst die dezelfde structuur heeft als de lijst die wordt geretourneerd door de functie <strong>SPLIT</strong>.</td>
</tr>
<tr>
<td>FIRST (lijst)</td>
<td>Retourneer de eerste record van de opgegeven lijst, als die record niet leeg is. Anders treedt een uitzondering op.</td>
<td></td>
</tr>
<tr>
<td>FIRSTORNULL (lijst)</td>
<td>Retourneer de eerste record van de opgegeven lijst, als die record niet leeg is. Retourneer anders een <strong>null</strong>-record.</td>
<td></td>
</tr>
<tr>
<td>LISTOFFIRSTITEM (lijst)</td>
<td>Retourneer een lijst die alleen het eerste item uit de opgegeven lijst bevat.</td>
<td></td>
</tr>
<tr>
<td>ALLITEMS (pad)</td>
<td>Deze functie wordt uitgevoerd als een selectie in het geheugen. De functie retourneert een nieuwe afgevlakte lijst die alle items vertegenwoordigt die overeenkomen met het opgegeven pad. Het pad moet worden gedefinieerd als een geldig gegevensbronpad van een gegevensbronelement van een recordlijstgegevenstype. Gegevenselementen zoals de padreeks en de datum moeten tijdens het ontwerp tot een fout leiden in de ER Expression Builder.</td>
<td>Als u <strong>SPLIT(&quot;abcdef&quot; , 2)</strong> als gegevensbron invoert, wordt met <strong>COUNT( ALLITEMS (DS.Value))</strong> <strong>3</strong> geretourneerd.</td>
</tr>
<tr>
<td>ALLITEMSQUERY (pad)</td>
<td>Deze functie wordt uitgevoerd als een gekoppelde SQL-query. De functie retourneert een nieuwe afgevlakte lijst die alle items vertegenwoordigt die overeenkomen met het opgegeven pad. Het opgegeven pad moet worden gedefinieerd als een geldig gegevensbronpad van een gegevensbronelement van het gegevenstype recordlijst en moet ten minste één relatie bevatten. Gegevenselementen zoals de padreeks en de datum moeten tijdens het ontwerp tot een fout leiden in de ER Expression Builder.</td>
<td>Definieer de volgende gegevensbronnen in uw modeltoewijzing:
<ul>
<li><strong>CustInv</strong> (type <strong>Tabelrecords</strong>), die verwijst naar de tabel CustInvoiceTable</li> 
<li><strong>FilteredInv</strong> (type <strong>Berekend veld</strong>), bevat de expressie <strong>FILTER (CustInv, CustInv.InvoiceAccount = &quot;US-001&quot;)</strong></li>
<li><strong>JourLines</strong> (type <strong>Berekend veld</strong>), bevat de expressie <strong>ALLITEMSQUERY (FilteredInv.'&lt;Relations. CustInvoiceJour.'&lt;Relations. CustInvoiceTrans)</strong></li>
</ul>
<p>Bij het uitvoeren van de modeltoewijzing om de gegevensbron <strong>JourLines</strong> aan te roepen, wordt de volgende SQL-instructie uitgevoerd:</p>
SELECT ... FROM CUSTINVOICETABLE T1 CROSS JOIN CUSTINVOICEJOUR T2 CROSS JOIN CUSTINVOICETRANS T3 WHERE...
</td>
</tr>
<tr>
<td>ORDERBY (lijst [, expressie 1, expressie 2, …])</td>
<td>De opgegeven lijst retourneren nadat deze is gesorteerd volgens de opgegeven argumenten. Deze argumenten kunnen worden gedefinieerd als een expressie.</td>
<td>Als <strong>Leverancier</strong> als een ER-gegevensbron wordt geconfigureerd die naar de tabel VendTable verwijst, retourneert <strong>ORDERBY (Leveranciers,Leverancier.'naam() ')</strong> de lijst met leveranciers die in oplopende volgorde op naam is gesorteerd.</td>
</tr>
<tr>
<td>REVERSE (lijst)</td>
<td>Retourneer de opgegeven lijst in omgekeerde sorteervolgorde.</td>
<td>Als <strong>Leverancier </strong> als een ER-gegevensbron wordt geconfigureerd die naar de tabel VendTable verwijst, retourneert <strong>REVERSE (ORDERBY (Leveranciers,Leverancier.'naam()')) )</strong> de lijst met leveranciers die in aflopende volgorde op naam is gesorteerd.</td>
</tr>
<tr>
<td>WHERE (lijst, voorwaarde)</td>
<td>De opgegeven lijst retourneren nadat deze is gefilterd volgens de opgegeven voorwaarde. De opgegeven voorwaarde wordt toegepast op de lijst in het geheugen. Hierin verschilt de functie <strong>WHERE</strong> van de functie <strong>FILTER</strong>.</td>
<td>Als <strong>Leverancier</strong> als een ER-gegevensbron wordt geconfigureerd die naar de tabel VendTable verwijst, wordt met <strong>WHERE(Vendors, Vendors.VendGroup = &quot;40&quot;)</strong> de lijst met leveranciers geretourneerd die behoren tot de leveranciersgroep 40.</td>
</tr>
<tr>
<td>ENUMERATE (lijst)</td>
<td>Retourneer een nieuwe lijst die bestaat uit opgesomde records van de opgegeven lijst en die de volgende elementen beschikbaar maakt:
<ul>
<li>Opgegeven lijstrecords als normale lijsten (component <strong>Waarde </strong>)</li>
<li>De huidige recordindex (onderdeel <strong>Nummer</strong>)</li>
</ul>
</td>
<td>In het volgende voorbeeld wordt de gegevensbron <strong>Genummerd</strong> gemaakt als een genummerde lijst leveranciersrecords van de gegevensbron <strong>Leveranciers</strong> die verwijst naar de tabel VendTable.
<p><a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a></p>
<p>In de volgende afbeelding ziet u de ontworpen indelingslay-out. In deze indeling worden gegevensbindingen gemaakt om uitvoer in XML-indeling te genereren. Deze uitvoer presenteert afzonderlijke leveranciers als opgesomde knooppunten.</p>
<p><a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a></p>
<p>In de volgende afbeelding ziet u het resultaat wanneer de ontworpen indeling wordt uitgevoerd.</p>
<a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a>
</td>
</tr>
<tr>
<td>COUNT (lijst)</td>
<td>Retourneer het aantal records in de opgegeven lijst, als de lijst niet leeg is. Retourneer anders <strong>0</strong> (nul).</td>
<td><strong>COUNT (SPLIT(&quot;abcd&quot; , 3))</strong> retourneert <strong>2</strong>, omdat de functie <strong>SPLIT</strong> een lijst maakt die uit twee records bestaat.</td>
</tr>
<tr>
<td>LISTOFFIELDS (pad)</td>
<td>Een lijst met records retourneren die is gemaakt op basis van een argument van een van de volgende typen:
<ul>
<li>Modelopsomming</li>
<li>Opsomming van indelingen</li>
<li>Container</li>
</ul>
<p>De lijst die wordt gemaakt bestaat uit records met de volgende velden:</p>
<ul>
<li>Naam</li>
<li>Label</li>
<li>Omschrijving</li>
</ul>
De velden <strong>Label</strong> en <strong>Omschrijving</strong> retourneren tijdens runtime waarden op basis van de taalinstellingen van de indeling.
</td>
<td>In het volgende voorbeeld wordt een opsomming geïntroduceerd in een gegevensmodel.
<p><a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="Enumeration in a model" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a></p>
<p>De volgende afbeelding toont deze details:</p>
<ul>
<li>De modelopsomming wordt in een rapport ingevoegd als gegevensbron.</li>
<li>Een ER-expressie gebruikt de modelopsomming als een parameter van de functie <strong>LISTOFFIELDS</strong>.</li>
<li>Een gegevensbron van het type recordlijst wordt ingevoegd in een rapport met de gemaakte ER-expressie.</li>
</ul>
<p><a href="./media/ger-listoffields-function-in-format-expression.png"><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="Format" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a></p>
<p>In het volgende voorbeeld ziet u de elementen van de ER-indeling die gebonden zijn aan de gegevensbron van het type recordlijst die is gemaakt met de functie <strong>LISTOFFIELDS</strong>.</p>
<p><a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="Format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a></p>
<p>In de volgende afbeelding ziet u het resultaat wanneer de ontworpen indeling wordt uitgevoerd.</p>
<p><a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="Format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a></p>
<blockquote>[!NOTE] Op basis van de taalinstellingen van de bovenliggende indelingselementen BESTAND en MAP worden labels en beschrijvingen in de uitvoer van de ER-indeling ingevoerd.</blockquote>
</td>
</tr>
<tr>
<td>LISTOFFIELDS (pad, taal)</td>
<td>Een lijst met records retourneren die is gemaakt op basis van een argument, zoals een modelopsomming, een indeling of een container. De lijst die wordt gemaakt bestaat uit records met de volgende velden:
<ul>
<li>Naam</li>
<li>Label</li>
<li>Omschrijving</li>
<li>Is vertaald</li>
</ul>
De velden <strong>Label</strong> en <strong>Omschrijving</strong> retourneren tijdens runtime waarden op basis van de taalinstellingen van de indeling en de opgegeven taal. Het veld <strong>Is vertaald</strong> geeft aan dat het veld <strong>Label</strong> in de opgegeven taal is vertaald.
</td>
<td>U gebruikt bijvoorbeeld het gegevensbrontype <strong>Berekend veld</strong> om de gegevensbronnen <strong>enumType_de</strong> en <strong>enumType_deCH</strong> te configureren voor de gegevensmodelopsomming <strong>enumType</strong>.
<ul>
<li>enumType_de = <strong>LISTOFFIELDS</strong> (enumType, &quot;de&quot;)</li>
<li>enumType_deCH = <strong>LISTOFFIELDS</strong> (enumType, &quot;de-CH&quot;)</li>
</ul>
<p>In dit geval kunt u de volgende expressie gebruiken om het label van de opsommingswaarde in Zwitsers Duits te krijgen, als deze vertaling beschikbaar is. Als de Zwitsers Duitse vertaling niet beschikbaar is, is het label in het Duits.</p>
IF (NOT (enumType_deCH.IsTranslated), enumType_de.Label, enumType_deCH.Label)
</td>
</tr>
<tr>
<td>STRINGJOIN (lijst, veldnaam, scheidingsteken)</td>
<td>Een tekenreeks retourneren die bestaat uit samengevoegde waarden van het opgegeven veld uit de opgegeven lijst. De waarden worden gescheiden door het opgegeven scheidingsteken.</td>
<td>Als u <strong>SPLIT(&quot;abc&quot; , 1)</strong> invoert als gegevensbron (DS), retourneert <strong>STRINGJOIN (DS, DS.Value, &quot;-&quot;)</strong> <strong>&quot;a-b-c&quot;</strong>.</td>
</tr>
<tr>
<td>SPLITLISTBYLIMIT (lijst, limietwaarde, limietbron)</td>
<td>Splitst de opgegeven lijst in een nieuwe lijst met sublijsten en retourneert het resultaat in recordlijstinhoud. De parameter <strong>limietwaarde</strong> definieert de waarde van de limiet om de lijst van herkomst te splitsen. De parameter voor de <strong>limietbron</strong> definieert de stap waarmee de totale som wordt verhoogd. De limiet wordt niet toegepast op één artikel van de oorspronkelijke lijst als de limietbron de gedefinieerde limiet overschrijdt.</td>
<td>In de volgende afbeelding ziet u een indeling. 
<p><a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="Format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a></p>
<p>In de volgende afbeelding ziet u de gegevensbronnen die voor de indeling worden gebruikt.</p>
<p><a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="Data sources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a></p>
<p>In de volgende afbeelding ziet u het resultaat wanneer de indeling wordt uitgevoerd. In dit geval is de uitvoer een platte lijst met basisproducten.</p>
<p><a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="Output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a></p>
<p>De volgende voorbeelden laten dezelfde indeling zien die is aangepast om de lijst met basisproducten in batches weer te geven wanneer één batch basisproducten moet omvatten en het totale gewicht niet groter mag zijn dan 9.</p>
<p><a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="Adjusted format" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a></p>
<p><a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="Data sources for the adjusted format" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a></p>
<p>In de volgende afbeelding ziet u het resultaat wanneer de aangepaste indeling wordt uitgevoerd.</p>
<p><a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="Output of the adjusted format" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a></p>
<blockquote>[!NOTE] De limiet wordt niet toegepast op het laatste artikel van de oorspronkelijke lijst omdat de waarde (11) van de limietbron (gewicht) de gedefinieerde limiet (9) overschrijdt. Gebruik de functie <strong>WHERE</strong> of de expressie <strong>Ingeschakeld</strong> van het bijbehorende indelingselement om de sublijsten te negeren (overslaan) tijdens het genereren van het rapport (indien nodig).</blockquote>
</td>
</tr>
<tr>
<td>FILTER (lijst, voorwaarde)</td>
<td>De opgegeven lijst retourneren nadat de query is gewijzigd om te filteren op de opgegeven voorwaarde. Deze functie verschilt van de functie <strong>WHERE</strong> omdat de opgegeven voorwaarde wordt toegepast op een ER-gegevensbron van het type <strong>Tabelrecords</strong> op het databaseniveau. De lijst en de voorwaarde kunnen worden gedefinieerd met behulp van tabellen en relaties.</td>
<td>Als <strong>Leverancier</strong> als een ER-gegevensbron wordt geconfigureerd die naar de tabel VendTable verwijst, wordt met <strong>FILTER(Vendors, Vendors.VendGroup = &quot;40&quot;)</strong> een lijst met leveranciers geretourneerd die behoren tot de leveranciersgroep 40. Als <strong>Vendor</strong> is geconfigureerd als een ER-gegevensbron die verwijst naar de tabel VendTable en als <strong>parmVendorBankGroup</strong> is geconfigureerd als een ER-gegevensbron die een waarde van het gegevenstype <strong>String</strong> retourneert, retourneert <strong>FILTER (Vendor.'&lt;Relations'.VendBankAccount, Vendor.'&lt;Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)</strong> een lijst met alleen de leveranciersaccounts die behoren tot een specifieke bankgroep.</td>
</tr>
<tr>
<td>INDEX (list, index)</td>
<td>Deze functie retourneert een record die wordt geselecteerd door een specifieke numerieke index in de lijst. Er wordt een uitzondering gegenereerd als de index zich buiten het bereik van de records in de lijst bevindt.</td>
<td>Als u de gegevensbron <strong>DS</strong> invoert voor het type <strong>Berekend veld</strong> en deze de expressie <strong>SPLIT ("A|B|C", “|”), 2</strong> bevat, retourneert de expressie <strong>DS.Value</strong> de tekstwaarde "B". De expressie <strong>INDEX (SPLIT ("A|B|C", “|”), 2).Value</strong> retourneert eveneens de tekstwaarde "B".</td>
</tr>
</tbody>
</table>

### <a name="logical-functions"></a>Logische functies

| Functie | Beschrijving | Voorbeeld |
|----------|-------------|---------|
| CASE (expressie, optie 1, resultaat 1 \[, optie 2, resultaat 2\] … \[, standaardresultaat\]) | Evalueer de opgegeven expressiewaarde tegen de opgegeven alternatieve opties. Retourneer het resultaat van de optie die gelijk is aan de waarde van de expressie. Retourneer anders het optionele standaardresultaat als een standaardresultaat is opgegeven. (Het standaardresultaat is de laatste parameter die niet wordt voorafgegaan door een optie.) | **CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")** retourneert de tekenreeks **"WINTER"** wanneer de datum van de huidige Finance and Operations-sessie tussen oktober en december is. Anders wordt een lege tekenreeks geretourneerd. |
| IF (voorwaarde, waarde 1, waarde 2) | Retourneer de eerste opgegeven waarde wanneer aan de opgegeven voorwaarde is voldaan. Anders wordt de tweede opgegeven waarde als resultaat gegeven. Als waarde 1 en waarde 2 records of recordlijsten zijn, bevat het resultaat alleen de velden die in beide lijsten bestaan. | **IF (1=2, "aan voorwaarde is voldaan", "aan voorwaarde is niet voldaan")** retourneert de tekenreeks **"aan voorwaarde is niet voldaan"**. |
| NOT (voorwaarde) | Retourneer de omgekeerde logische waarde van de opgegeven voorwaarde. | **NOT (WAAR)** retourneert **FALSE**. |
| AND (voorwaarde 1\[, voorwaarde 2, ...\]) | Retourneer **TRUE** als *alle* opgegeven voorwaarden waar zijn. Retourneer anders **FALSE**. | **AND (1=1, "a"="a")** retourneert **TRUE**. **AND (1=2, "a"="a")** retourneert **FALSE**. |
| OR (voorwaarde 1\[, voorwaarde 2, ...\]) | Retourneer **FALSE** als *alle* opgegeven voorwaarden onwaar zijn. Retourneer **TRUE** als *een van de* opgegeven voorwaarden waar is. | **OR (1=2, "a"="a")** retourneert **TRUE**. |
| VALUEIN (invoer, lijst, lijstitemexpressie) | Bepalen of de opgegeven invoer overeenkomt met een waarde van een item in de opgegeven lijst. **TRUE** retourneren als de opgegeven invoer overeenkomt met het resultaat van het uitvoeren van de opgegeven expressie voor ten minste één record. Retourneer anders **FALSE**. De **invoer**parameter vertegenwoordigt het pad van een gegevensbronelement. De waarde van dit element wordt vergeleken. De **lijst**parameter vertegenwoordigt het pad van een gegevensbronelement van het type recordlijst als een lijst met records die een expressie bevat. De waarde van dit element wordt vergeleken met de opgegeven invoer. Het argument **lijstitemexpressie** vertegenwoordigt een expressie die verwijst naar of bevat een enkel veld van de opgegeven lijst dat moet worden gebruikt voor de vergelijking. | Zie voor voorbeelden de volgende sectie [Voorbeelden: VALUEIN (invoer, lijst, lijstitemexpressie)](#examples-valuein-input-list-list-item-expression). |

#### <a name="examples-valuein-input-list-list-item-expression"></a>Voorbeelden: VALUEIN (invoer, lijst, lijstitemexpressie)
In het algemeen wordt de functie **VALUEIN** omgezet in een reeks **OF**-voorwaarden:

(invoer = lijst.item1.value) OF (invoer = lijst.item2.value) OF ...

##### <a name="example-1"></a>Voorbeeld 1
U definieert de volgende gegevensbron in uw modeltoewijzing: **Lijst** (type **Berekend veld**). Deze gegevensbron bevat de expressie **SPLIT ("a,b,c", ",")**.

Als een gegevensbron wordt aangeroepen die is geconfigureerd als de expressie **VALUEIN ("B", list, List.Value)**, wordt **TRUE** geretourneerd. In dit geval wordt de functie **VALUEIN** omgezet in de volgende reeks voorwaarden:

**(("B" = "a") of ("B" = "b") of ("B" = "c"))**, waarbij **("B" = "b")** gelijk is aan **TRUE**

Als een gegevensbron wordt aangeroepen die is geconfigureerd als de expressie **VALUEIN ("B", List, LEFT(List.Value, 0))**, wordt **FALSE** geretourneerd. In dit geval wordt de functie **VALUEIN** omgezet in de volgende voorwaarde:

**("B" = "")**, wat niet gelijk is aan **TRUE**

Houd er rekening mee dat de bovengrens voor het aantal tekens in de tekst van een dergelijke voorwaarde 32.768 tekens is. Daarom moet u geen gegevensbronnen maken die deze limiet tijdens de uitvoering mogelijk overschrijden. Als de limiet wordt overschreden, stopt de uitvoering van de toepassing en treedt een uitzondering op. Deze situatie kan zich bijvoorbeeld voordoen als de gegevensbron is geconfigureerd as **WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)** en de lijsten **List1** en **List2** een groot aantal records bevatten.

In sommige gevallen moet de functie **VALUEIN** worden omgezet in een database-instructie met behulp van de operator **EXISTS JOIN**. Dit probleem treedt op wanneer de functie **FILTER** wordt gebruikt en aan de volgende voorwaarden wordt voldaan:

- De optie **VRAGEN OM QUERY** is uitgeschakeld voor de gegevensbron van de functie **VALUEIN** die naar de lijst met records verwijst. (Er worden tijdens de uitvoering geen extra voorwaarden op deze gegevensbron toegepast.)
- Er worden geen geneste expressies geconfigureerd voor de gegevensbron van de functie **VALUEIN** die naar de lijst met records verwijst.
- Een item in de lijst van de functie **VALUEIN** verwijst naar een veld (niet een expressie of een methode) van de opgegeven gegevensbron.

Overweeg deze optie te gebruiken in plaats van de functie **WHERE**, zoals eerder in dit voorbeeld beschreven.

##### <a name="example-2"></a>Voorbeeld 2

U definieert de volgende gegevensbronnen in uw modeltoewijzing:

- **In** (type **Tabelrecords**), dat verwijst naar de tabel Intrastat
- **Port** (type **Tabelrecords**), dat verwijst naar de tabel IntrastatPort

Wanneer een gegevensbron wordt aangeroepen die is geconfigureerd als de expressie **FILTER (In, VALUEIN(In.Port, Port, Port.PortId)**, wordt de volgende SQL-instructie gegenereerd om gefilterde records van de tabel Intrastat te retourneren:

```
select … from Intrastat
exists join TableId from IntrastatPort
where IntrastatPort.PortId = Intrastat.Port
```

Voor **dataAreaId**-velden wordt de uiteindelijke SQL-instructie gegenereerd via de operator **IN**.

##### <a name="example-3"></a>Voorbeeld 3

U definieert de volgende gegevensbronnen in uw modeltoewijzing:

- **Le** (type **Berekend veld**), dat de expressie **SPLIT ("DEMF,GBSI,USMF", ",")** bevat
- **In** (type **Tabelrecords**), dat verwijst naar de tabel Intrastat en waarvoor de optie **Hele bedrijf** is ingeschakeld

Wanneer een gegevensbron wordt aangeroepen die is geconfigureerd als de expressie **FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)**, bevat de uiteindelijke SQL-instructie de volgende voorwaarde:

```
Intrastat.dataAreaId IN ('DEMF', 'GBSI', 'USMF')
```

### <a name="mathematical-functions"></a>Wiskundige functies

| Functie | Omschrijving | Voorbeeld |
|----------|-------------|---------|
| ABS (getal) | De absolute waarde van het opgegeven getal retourneren. (Met andere woorden: het getal zonder teken retourneren.) | **ABS (-1)** retourneert **1**. |
| POWER (aantal, macht) | Retourneert het resultaat van het verheffen van het opgegeven positieve getal naar de opgegeven macht. | **POWER (10, 2)** retourneert **100**. |
| NUMBERVALUE (tekenreeks, decimaal scheidingsteken, scheidingsteken groep komma) | Converteert de opgegeven tekenreeks naar een getal. Het opgegeven decimaalteken wordt gebruikt tussen het geheel-getaldeel en het breukdeel van een decimaal getal. Het opgegeven scheidingsteken voor cijfergroepering wordt gebruikt als scheidingsteken voor duizendtallen. | **NUMBERVALUE (1", "234,56 ",", "")** retourneert de waarde **1234,56**. |
| VALUE (tekenreeks) | Converteert de opgegeven tekenreeks naar een getal. De komma's en punttekens (.) worden beschouwd als decimale scheidingstekens en er wordt een koppelteken (-) vooraan gebruikt als minteken. Er treedt een uitzondering op als andere niet-numerieke tekens worden aangetroffen in de opgegeven tekenreeks. | **VALUE ("1" 234,56)** geeft een uitzondering. |
| ROUND (getal, decimalen) | Retourneer het opgegeven getal nadat het is afgerond op het opgegeven aantal decimalen:<ul><li>Als de waarde van de parameter **decimalen** groter is dan 0 (nul), wordt het opgegeven getal afgerond op dat aantal decimalen.</li><li>Als de waarde van de parameter **decimalen** **0** (nul) is, wordt het opgegeven getal afgerond op het dichtstbijzijnde hele getal.</li><li>Als de waarde van de parameter **decimalen** minder dan 0 (nul) is, wordt het opgegeven getal links van de decimale komma afgerond.</li></ul> | **ROUND (1200,767, 2)** rondt af naar twee decimalen en retourneert **1200,77**. **ROUND (1200,767, -3)** rondt af naar het dichtstbijzijnde veelvoud van 1.000 en retourneert **1000**. |
| ROUNDDOWN (getal, decimalen) | Retourneer het opgegeven getal nadat het is afgerond omlaag op het opgegeven aantal decimalen.<blockquote>[!NOTE] Deze functie werkt als **ROUND**, maar rondt altijd het opgegeven getal naar beneden af (richting nul).</blockquote> | **ROUNDDOWN (1200,767, 2)** rondt naar beneden af naar twee decimalen en retourneert **1200,76**. **ROUNDDOWN (1700,767, -3)** rondt naar beneden af naar het dichtstbijzijnde veelvoud van 1.000 en retourneert **1000**. |
| ROUNDUP (getal, decimalen) | Retourneer het opgegeven getal nadat het naar boven is afgerond op het opgegeven aantal decimalen.<blockquote>[!NOTE] Deze functie werkt als **ROUND**, maar rondt altijd het opgegeven getal naar boven af (weg van nul).</blockquote> | **ROUNDUP (1200,763, 2)** rondt naar boven af naar twee decimalen en retourneert **1200,77**. **ROUNDUP (1200,767, -3)** rondt naar boven af naar het dichtstbijzijnde veelvoud van 1.000 en retourneert **2000**. |

### <a name="data-conversion-functions"></a>Functies voor gegevensconversie

| Functie | Omschrijving | Voorbeeld |
|----------|-------------|---------|
| VALUE (tekenreeks) | Converteert de opgegeven tekenreeks naar een getal. De komma's en punttekens (.) worden beschouwd als decimale scheidingstekens en er wordt een koppelteken (-) vooraan gebruikt als minteken. Er treedt een uitzondering op als andere niet-numerieke tekens worden aangetroffen in de opgegeven tekenreeks. | **VALUE ("1" 234,56)** geeft een uitzondering. |
| NUMBERVALUE (tekenreeks, decimaal scheidingsteken, scheidingsteken groep komma) | Converteert de opgegeven tekenreeks naar een getal. Het opgegeven decimaalteken wordt gebruikt tussen het geheel-getaldeel en het breukdeel van een decimaal getal. Het opgegeven scheidingsteken voor cijfergroepering wordt gebruikt als scheidingsteken voor duizendtallen. | **NUMBERVALUE("1 234,56", ",", " ")** retourneert **1234.56**. |
| INTVALUE (tekenreeks) | Een geheel-getalweergave van de opgegeven tekenreeks retourneren. Eventuele cijfers achter de komma worden afgekapt. | **INTVALUE ("100.77")** retourneert **100**. |
| INTVALUE (getal) | Een geheel-getalweergave van het opgegeven getal retourneren. Eventuele cijfers achter de komma worden afgekapt. | **INTVALUE (-100.77)** retourneert **-100**. |
| INT64VALUE (tekenreeks) | Een int64-weergave van de opgegeven tekenreeks retourneren. Eventuele cijfers achter de komma worden afgekapt. | **INT64VALUE ("22565422744")** retourneert **22565422744**. |
| INT64VALUE (getal) | Een int64-weergave van het opgegeven getal retourneren. Eventuele cijfers achter de komma worden afgekapt. | **INT64VALUE (22565422744.00)** retourneert **22565422744**. |

### <a name="record-functions"></a>Registratiefuncties

| Functie | Omschrijving | Voorbeeld |
|----------|-------------|---------|
| NULLCONTAINER (lijst) | Retourneer een **null**-record met dezelfde structuur als de opgegeven recordlijst of record.<blockquote>[!NOTE] Deze functie is verouderd. Gebruik in plaats daarvan **EMPTYRECORD**.</blockquote> | **NULLCONTAINER (SPLIT ("abc", 1))** retourneert een nieuwe lege record die dezelfde structuur heeft als de lijst die wordt geretourneerd door de functie **SPLIT**. |
| EMPTYRECORD (record) | Retourneer een **null**-record met dezelfde structuur als de opgegeven recordlijst of record.<blockquote>[!NOTE] Een **null**-record is een record waarin alle velden een lege waarde hebben. Een lege waarde is **0** (nul) voor getallen, een lege tekenreeks voor tekenreeksen, enzovoort.</blockquote> | **EMPTYRECORD (SPLIT ("abc", 1))** retourneert een nieuwe lege record die dezelfde structuur heeft als de lijst die wordt geretourneerd door de functie **SPLIT**. |

### <a name="text-functions"></a>Tekstfuncties

<table>
<thead>
<tr>
<th>Functie</th>
<th>Omschrijving</th>
<th>Voorbeeld</th>
</tr>
</thead>
<tbody>
<tr>
<td>UPPER (tekenreeks)</td>
<td>Retourneer de opgegeven tekenreeks nadat deze is geconverteerd naar hoofdletters.</td>
<td><strong>UPPER(&quot;Voorbeeld&quot;)</strong> retourneert <strong>&quot;VOORBEELD&quot;</strong>.</td>
</tr>
<tr>
<td>LOWER (tekenreeks)</td>
<td>Retourneer de opgegeven tekenreeks nadat deze is geconverteerd naar kleine letters.</td>
<td><strong>LOWER (&quot;Voorbeeld&quot;)</strong> retourneert <strong>&quot;voorbeeld&quot;</strong>.</td>
</tr>
<tr>
<td>LEFT (tekenreeks, aantal tekens)</td>
<td>Retourneer het opgegeven aantal tekens vanaf het begin van de opgegeven tekenreeks.</td>
<td><strong>LEFT (&quot;Voorbeeld&quot;, 3)</strong> retourneert <strong>&quot;Voo&quot;</strong>.</td>
</tr>
<tr>
<td>RIGHT (tekenreeks, aantal tekens)</td>
<td>Retourneer het opgegeven aantal tekens vanaf het eind van de opgegeven tekenreeks.</td>
<td><strong>RIGHT (&quot;Voorbeeld&quot;, 3)</strong> retourneert <strong>&quot;eld&quot;</strong>.</td>
</tr>
<tr>
<td>MID (tekenreeks, beginpositie, aantal tekens)</td>
<td>Retourneer het opgegeven aantal tekens van de opgegeven tekenreeks, vanaf de opgegeven positie.</td>
<td><strong>MID (&quot;Voorbeeld&quot;, 2, 3)</strong> retourneert <strong>&quot;oor&quot;</strong>.</td>
</tr>
<tr>
<td>LEN (tekenreeks)</td>
<td>Retourneer het aantal tekens in de opgegeven tekenreeks.</td>
<td><strong>LEN (&quot;Voorbeeld&quot;)</strong> retourneert <strong>6</strong>.</td>
</tr>
<tr>
<td>CHAR (getal)</td>
<td>Retourneer de tekenreeks waarnaar wordt verwezen door het opgegeven Unicode-getal.</td>
<td><strong>CHAR (255)</strong> retourneert <strong>&quot;ÿ&quot;</strong>.
<blockquote>[!NOTE] De door deze functie geretourneerde tekenreeks is afhankelijk van de codering die in het bovenliggende FILE-indelingselement is geselecteerd. Zie voor een overzicht van ondersteunde coderingen, <a href="https://msdn.microsoft.com/en-us/library/system.text.encoding(v=vs.110).aspx">Codering klasse</a>.</blockquote>
</td>
</tr>
<tr>
<td>CONCATENATE (tekenreeks 1 [, tekenreeks 2, …])</td>
<td>Retourneer alle opgegeven tekenreeksen nadat deze zijn samengevoegd in één tekenreeks.</td>
<td><strong>CONCATENATE (&quot;abc&quot;, &quot;def&quot;)</strong> retourneert <strong>&quot;abcdef&quot;</strong>.
<blockquote>[!NOTE] De expressie <strong>&quot;abc&quot; &amp; &quot;def&quot;</strong> retourneert ook <strong>&quot;abcdef&quot;</strong>.</blockquote>
</td>
</tr>
<tr>
<td>TRANSLATE (tekenreeks, patroon, vervanging)</td>
<td>Retourneer de opgegeven tekenreeks nadat alle gevonden tekens in de opgegeven patroontekenreeks zijn vervangen door de tekens op de bijbehorende positie van de opgegeven vervangingstekenreeks.</td>
<td><strong>TRANSLATE (&quot;abcdef&quot;, &quot;cd&quot;, &quot;GH&quot;)</strong> vervangt het patroon <strong>&quot;cd&quot;</strong> door de tekenreeks <strong>&quot;GH&quot;</strong> en retourneert <strong>&quot;abGHef&quot;</strong>.</td>
</tr>
<tr>
<td>REPLACE (tekenreeks, patroon, vervanging, normale-expressiemarkering)</td>
<td>Wanneer de opgegeven parameter <strong>normale-expressiemarkering</strong> <strong>waar</strong> is, de opgegeven tekenreeks retourneren nadat deze is gewijzigd door de normale expressie toe te passen die als <strong>patroon</strong>argument voor deze functie wordt opgegeven. Deze expressie wordt gebruikt om tekens te zoeken die moeten worden vervangen. Tekens van het opgegeven <strong>vervanging</strong>sargument worden gebruikt om tekens te vervangen die zijn gevonden. Wanneer de opgegeven <strong>normale-expressiemarkering</strong> <strong>false</strong> is, gedraagt deze functie zich als <strong>TRANSLATE</strong>.</td>
<td><strong>REPLACE (&quot;+1 923 456 4971&quot;, &quot;[^0-9]&quot;, &quot;&quot;, true)</strong> past een normale expressie toe waarmee alle niet-numerieke symbolen worden verwijderd, en retourneert <strong>&quot;19234564971&quot;</strong>. <strong>REPLACE (&quot;abcdef&quot;, &quot;cd&quot;, &quot;GH&quot;, false)</strong> vervangt het patroon <strong>&quot;cd&quot;</strong> door de tekenreeks <strong>&quot;GH&quot;</strong> en retourneert <strong>&quot;abGHef&quot;</strong>.</td>
</tr>
<tr>
<td>TEXT (invoer)</td>
<td>Retourneer de opgegeven invoer nadat deze is geconverteerd naar een tekenreeks die wordt opgemaakt volgens de lokale instellingen van de server van het huidige Finance and Operations-exemplaar. Voor waarden van het type <strong>real</strong> wordt de tekenreeksconversie beperkt tot twee decimalen.</td>
<td>Als de landinstelling van de server van het Finance and Operations-exemplaar is gedefinieerd als <strong>EN-US</strong>, retourneert <strong>TEXT (NOW ())</strong> de datum van de huidige Finance and Operations-sessie, 17 december 2015, als de tekenreeks <strong>&quot;12/17/2015 07:59:23 AM&quot;</strong>. <strong>TEXT (1/3)</strong> retourneert <strong>&quot;0.33&quot;</strong>.</td>
</tr>
<tr>
<td>FORMAT (tekenreeks 1, tekenreeks 2[, tekenreeks 3, ...])</td>
<td>Retourneer de opgegeven tekenreeks nadat deze is opgemaakt door elk exemplaar van <strong>%N</strong> te vervangen door het <em>n</em>de argument. De argumenten zijn tekenreeksen. Als een argument niet voor een parameter wordt verstrekt, wordt de parameter geretourneerd als <strong>&quot;%N&quot;</strong> in de tekenreeks. Voor waarden van het type <strong>real</strong> wordt de tekenreeksconversie beperkt tot twee decimalen.</td>
<td>In het volgende voorbeeld retourneert de gegevensbron <strong>PaymentModel</strong> de lijst van klantrecords via het onderdeel <strong>Klant</strong> en de waarde van de verwerkingsdatum via het veld <strong>ProcessingDate</strong>.
<p><a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a></p>
<p>In de ER-indeling die is ontworpen om een elektronisch bestand voor geselecteerde klanten te genereren, wordt  <strong>PaymentModel</strong> geselecteerd als een gegevensbron en beheert deze de processtroom. Er treedt een uitzondering om de gebruiker te informeren wanneer een geselecteerde klant wordt gestopt voor de datum waarop het rapport wordt verwerkt. De formule die is ontworpen voor dit type verwerkingsbesturingselement kan de volgende bronnen gebruiken:</p>
<ul>
<li>Finance and Operations-label SYS70894, met de volgende tekst:
<ul>
<li><strong>Voor de taal EN-US:</strong> &quot;Nothing to print&quot;</li>
<li><strong>Voor de taal NL:</strong> &quot;Er is niets om af te drukken&quot;</li>
</ul></li>
<li>Finance and Operations-label SYS18389, met de volgende tekst:
<ul>
<li><strong>Voor de taal EN-US:</strong> &quot;Customer %1 is stopped for %2&quot;</li>
<li><strong>Voor de taal DE:</strong> &quot;Debitor '%1' wird für %2 gesperrt.&quot;</li>
</ul></li>
</ul>
<p>Hier is de formule die kan worden ontworpen:</p>
<p>FORMAT (CONCATENATE (@&quot;SYS70894&quot;, &quot;. &quot;, @&quot;SYS18389&quot;), model.Customer.Name, DATETIMEFORMAT (model.ProcessingDate, &quot;d&quot;))</p>
<p>Als een rapport wordt verwerkt voor de klant <strong>Litware Retail</strong> op 17 december 2015 in de cultuur <strong>EN-US</strong> en de taal <strong>EN-US</strong>, retourneert deze formule de volgende tekst, die aan de gebruiker kan worden weergegeven als uitzonderingsbericht:</p>
<p>&quot;Er is niets om af te drukken. Customer Litware Retail is stopped for 12/17/2015."&quot;</p>
<p>Als hetzelfde rapport voor de klant <strong>Litware Retail</strong> wordt verwerkt op 17 december 2015 in de cultuur <strong>DE</strong> en de taal <strong>DE</strong>, retourneert de formule de volgende tekst die een andere datumnotatie gebruikt:</p>
<p>&quot;Nichts zu drucken. Klant "Litware Retail" is gestopt voor 17-12-2015.&quot;</p>
<blockquote>[!NOTE] De volgende syntaxis wordt toegepast in ER-formules voor labels:
<ul>
<li><strong>Voor labels van Finance and Operations-resources:</strong> <strong>@&quot;X&quot;</strong>, waarbij <strong>X</strong> de label-id in de Application Object Tree (AOT) is</li>
<li><strong>Voor labels die zich in ER-configuraties bevinden:</strong> <strong>@&quot;GER_LABEL:X&quot;</strong>, waarbij <strong>X</strong> de label-id in de ER-configuratie is</li>
</ul>
</blockquote>
</td>
</tr>
<tr>
<td>NUMBERFORMAT (getal, indeling)</td>
<td>Retourneer een tekenreeksvoorstelling van het opgegeven getal in de opgegeven indeling. (Zie voor informatie over de ondersteunde indelingen <a href="https://msdn.microsoft.com/en-us/library/dwhawy9k(v=vs.110).aspx">standaard</a> en <a href="https://msdn.microsoft.com/en-us/library/0c899ak8(v=vs.110).aspx">aangepast</a>.) De context waarin deze functie wordt uitgevoerd, bepaalt de cultuur die wordt gebruikt voor het opmaken van nummers.</td>
<td>Voor de cultuur EN-US retourneert <strong>NUMBERFORMAT (0.45, &quot;p&quot;)</strong> <strong>&quot;45.00 %&quot;</strong>. <strong>NUMBERFORMAT (10.45, &quot;#&quot;)</strong> retourneert <strong>&quot;10&quot;</strong>.</td>
</tr>
<tr>
<td>NUMERALSTOTEXT (aantal, taal, valuta, naamvlag van valuta afdrukken, aantal decimalen)</td>
<td>Het opgegeven getal retourneren nadat het is uitgeschreven (geconverteerd naar tekenreeksen) in de opgegeven taal. De taalcode is optioneel. Wanneer deze is gedefinieerd als een lege tekenreeks, wordt de taalcode voor de actieve context gebruikt. (De taalcode voor de actieve context is gedefinieerd voor een genererend bestand of map.) De valutacode is ook optioneel. Wanneer deze als lege tekenreeks is gedefinieerd, wordt de bedrijfsvaluta gebruikt.
<blockquote>[!NOTE] De parameters voor de <strong>vlag valutanaam afdrukken</strong> en de <strong>decimalen</strong> worden alleen geanalyseerd voor de volgende taalcodes: <strong>CS</strong>, <strong>ET</strong>, <strong>HU</strong>, <strong>LT</strong>, <strong>LV</strong>, <strong>PL</strong> en <strong>RU</strong>. De <strong>vlag voor valutanaam afdrukken</strong> wordt bovendien alleen geanalyseerd voor Finance and Operations-bedrijven waarbij de context van het land of de regio verbuiging van valutanamen ondersteunt.</blockquote>
</td>
<td><strong>NUMERALSTOTEXT (1234.56, &quot;EN&quot;, &quot;&quot;, false, 2)</strong> retourneert <strong>&quot;One Thousand Two Hundred Thirty Four and 56&quot;</strong>. <strong>NUMERALSTOTEXT (120, &quot;PL&quot;, &quot;&quot;, false, 0)</strong> retourneert <strong>&quot;Sto dwadzieścia&quot;</strong>. <strong>NUMERALSTOTEXT (120.21, &quot;RU&quot;, &quot;EUR&quot;, true, 2)</strong> retourneert <strong>&quot;Сто двадцать евро 21 евроцент&quot;</strong>.</td>
</tr>
<tr>
<td>PADLEFT (tekenreeks, lengte, opvultekens)</td>
<td>Retourneert een tekenreeks met de opgegeven lengte waarbij het begin van de opgegeven tekenreeks is aangevuld met de opgegeven tekens.</td>
<td><strong>PADLEFT (&quot;1234&quot;, 10, &quot;&nbsp;&quot;)</strong> retourneert de tekstreeks <strong>&quot;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234&quot;</strong>.</td>
</tr>
<tr>
<td>TRIM (tekenreeks)</td>
<td>De opgegeven tekenreeks retourneren nadat voorloopspaties en volgspaties zijn afgekapt en nadat meerdere spaties tussen woorden zijn verwijderd.</td>
<td><strong>TRIM (&quot;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Sample&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;text&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&quot;)</strong> retourneert <strong>&quot;Sample text&quot;</strong>.</td>
</tr>
<tr>
<td>GETENUMVALUEBYNAME (bronpad opsommingsgegevens, labeltekst opsommingswaarde)</td>
<td>Retourneert een waarde van de opgegeven opsommingsgegevensbron, op basis van de opgegeven tekst van het opsommingslabel.</td>
<td>In het volgende voorbeeld wordt de opsomming <strong>ReportDirection</strong> geïntroduceerd in een gegevensmodel. Houd er rekening mee dat labels voor opsommingswaarden worden gedefinieerd.
<p><a href="./media/ER-data-model-enumeration-values.PNG"><img src="./media/ER-data-model-enumeration-values.PNG" alt="Available values for data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a></p>
<p>De volgende afbeelding toont deze details:</p>
<ul>
<li>De modelopsomming <strong>ReportDirection</strong> wordt in een rapport ingevoegd als gegevensbron, <strong>$Direction</strong></li>
<li>Een ER-expressie <strong>$IsArrivals</strong> is ontworpen om de modelopsomming als parameter voor deze functie te gebruiken. De waarde van deze expressie is <strong>TRUE</strong>.</li>
</ul>
<a href="./media/ER-data-model-enumeration-usage.PNG"><img src="./media/ER-data-model-enumeration-usage.PNG" alt="Example of data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>
</td>
</tr>
<tr>
<td>GUIDVALUE (invoer)</td>
<td>Converteren van de opgegeven invoer van het gegevenstype <strong>String</strong> naar een gegevensitem van het gegevenstype <strong>GUID</strong>.<blockquote>[!NOTE] Als u een conversie in de tegenovergestelde richting wilt uitvoeren (dat wil zeggen: opgegeven invoer van het gegevenstype <strong>GUID</strong> converteren naar een gegevensitem van het gegevenstype <strong>Tekenreeks</strong>), kunt u de functie <strong>TEXT()</strong> gebruiken.</blockquote></td>
<td>U definieert de volgende gegevensbronnen in uw modeltoewijzing:
<ul>
<li><strong>myID</strong> (type <strong>Berekend veld</strong>), bevat de expressie <strong>GUIDVALUE (&quot;AF5CCDAC-F728-4609-8C8B-A4B30B0C0AA0&quot;)</strong></li>
<li><strong>Users</strong> (type <strong>Tabelrecords</strong>),verwijst naar de tabel UserInfo</li>
</ul>
Wanneer deze gegevensbronnen zijn gedefinieerd, kunt u een expressie zoals <strong>FILTER (Users, Users.objectId = myID)</strong> gebruiken om de tabel UserInfo te filteren op het veld <strong>objectId</strong> van het gegevenstype <strong>GUID</strong>.
</td>
</tr>
<tr>
<td>JSONVALUE (id, pad)</td>
<td>Parseren van gegevens in de indeling JavaScript Object Notation (JSON), die wordt bereikt met het opgegeven pad, om een scalaire waarde te extraheren die is gebaseerd op de opgegeven id.</td>
<td>De gegevensbron <strong>$JsonField</strong> bevat de volgende gegevens in JSON-indeling: <strong>{&quot;BuildNumber&quot;:&quot;7.3.1234.1&quot;,&quot;KeyThumbprint&quot;:&quot;7366E&quot;}</strong>. Voor deze gegevensbron retourneert </strong>JSONVALUE ( &quot;BuildNumber&quot;, $JsonField)</strong> de waarde <strong>7.3.1234.1</strong> van het gegevenstype <strong>String</strong>.</td>
</tr>
</tbody>
</table>

### <a name="data-conversion-functions"></a>Functies voor gegevensconversie

| Functie | Omschrijving | Voorbeeld |
|----------|-------------|---------|
| TEXT (invoer) | Retourneer de opgegeven invoer nadat deze is geconverteerd naar een tekenreeks die wordt opgemaakt volgens de lokale instellingen van de server van het huidige Finance and Operations-exemplaar. Voor waarden van het type **real** wordt de tekenreeksconversie beperkt tot twee decimalen. | Als de landinstelling van de server van het Finance and Operations-exemplaar is gedefinieerd als **EN-US**, retourneert **TEXT (NOW ())** de datum van de huidige Finance and Operations-sessie, 17 december 2015, als de tekenreeks **12/17/2015 07:59:23 AM**. **TEXT (1/3)** retourneert **"0,33"**. |
| QRCODE (tekenreeks) | Een Quick Response-code (QR-code) retourneren in binaire base64-indeling voor de opgegeven tekenreeks. | **QRCODE ("Sample text")** retourneert **U2FtcGxlIHRleHQ=**. |

### <a name="data-collection-functions"></a>Functies voor gegevensverzameling

| Functie | Omschrijving | Voorbeeld |
|----------|-------------|---------|
| FORMATELEMENTNAME () | Retourneert de naam van het element van de huidige indeling. Retourneert een lege tekenreeks wanneer de vlag **Uitvoerdetails verzamelen** van de huidige bestanden is uitgeschakeld. | Als u meer wilt weten over het gebruik van deze functie, raadpleegt u de taakbegeleiding **ER Gegevens van indelingsuitvoer gebruiken voor tellen en optellen**, die deel uitmaakt van het bedrijfsproces **Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen**. |
| SUMIFS (sleutelreeks voor optelling, tekenreeks criteriumbereik1, tekenreeks criteriumwaarde1 \[, tekenreeks criteriumbereik2, tekenreeks criteriumwaarde2 tekenreeks, …\]) | Een som retourneren met waarden die zijn verzameld uit XML-knooppunten (met als sleutel gedefinieerde naam) toen de indeling werd uitgevoerd en die voldoet aan de opgegeven voorwaarden (paren van bereiken en waarden). Retourneert een **0** (nul) wanneer de vlag **Uitvoerdetails verzamelen** van de huidige bestanden is uitgeschakeld. | |
| SUMIF (sleutelreeks voor optellen, criteriumbereik tekenreeks, criteriumwaarde tekenreeks) | De som retourneren van waarden die zijn verzameld uit XML-knooppunten (met als sleutel gedefinieerde naam) toen de indeling werd uitgevoerd en die voldoet aan de opgegeven voorwaarde (een bereik en een waarde). Retourneert een **0** (nul) wanneer de vlag **Uitvoerdetails verzamelen** van de huidige bestanden is uitgeschakeld. | |
| COUNTIFS (tekenreeks criteriumbereik1, tekenreeks criteriumwaarde1 \[, tekenreeks criteriumbereik2, tekenreeks criteriumwaarde2, …\]) | Het aantal XML-knooppunten retourneren dat is verzameld toen de indeling werd uitgevoerd en dat voldoet aan de opgegeven voorwaarden (paren bereiken en waarden). Retourneert een **0** (nul) wanneer de vlag **Uitvoerdetails verzamelen** van de huidige bestanden is uitgeschakeld. | |
| COUNTIF (criteriumbereik tekenreeks, criteriumwaarde tekenreeks) | Het aantal XML-knooppunten retourneren dat is verzameld toen de indeling werd uitgevoerd en dat voldoet aan de opgegeven voorwaarde (een bereik en een waarde). Retourneert een **0** (nul) wanneer de vlag **Uitvoerdetails verzamelen** van de huidige bestanden is uitgeschakeld. | |
| COLLECTEDLIST (tekenreeks criteriumbereik1, tekenreeks criteriumwaarde1 \[, tekenreeks criteriumbereik2, tekenreeks criteriumwaarde2, …\]) | De lijst met waarden retourneren die is verzameld voor XML-knooppunten toen de indeling werd uitgevoerd en die voldoet aan de opgegeven voorwaarden (een bereik en een waarde). Retourneert een lege lijst wanneer de vlag **Uitvoerdetails verzamelen** van de huidige bestanden is uitgeschakeld. | |

### <a name="other-business-domainspecific-functions"></a>Andere functies (voor specifiek zakelijk domein)

| Functie | Omschrijving | Voorbeeld |
|----------|-------------|---------|
| CONVERTCURRENCY (bedrag, bronvaluta, doelvaluta, datum, bedrijf) | Converteer het opgegeven monetaire bedrag van de opgegeven bronvaluta naar de opgegeven doelvaluta door de instellingen van het opgegeven Finance and Operations-bedrijf op de opgegeven datum te gebruiken. | **CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")** retourneert het equivalent van één euro in Amerikaanse dollars op de huidige sessiedatum, op basis van de instellingen voor het bedrijf DEMF. |
| ROUNDAMOUNT (aantal, decimalen, afrondingsregel) | Rond het opgegeven bedrag af op het opgegeven aantal decimalen, op basis van de opgegeven afrondingsregel.<blockquote>[!NOTE] De afrondingsregel moet worden opgegeven als een waarde van de Finance and Operations-opsomming **RoundOffType**.</blockquote> | Als de parameter **model.RoundOff** is ingesteld op **Downward**, retourneert **ROUNDAMOUNT (1000,787, 2, model.RoundOff)** de waarde **1000,78**. Als de parameter **model.RoundOff** is ingesteld op **Normal** of **Rounding-up**, retourneert **ROUNDAMOUNT (1000,787, 2, model.RoundOff)** de waarde **1000,79**. |
| CURCredRef (cijfers) | Retourneer een crediteurverwijzing op basis van de cijfers van het opgegeven factuurnummer. | **CURCredRef ("VEND-200002")** retourneert **"2200002"**. |
| MOD\_97 (cijfers) | Retourneer een crediteurverwijzing als een MOD97-expressie op basis van de cijfers van het opgegeven factuurnummer. | **MOD\_97 ("VEND-200002")** retourneert **"20000285"**. |
| ISOCredRef (cijfers) | Een ISO-crediteurverwijzing (International Organization for Standardization) retourneren op basis van de cijfers en alfabetische symbolen van het opgegeven factuurnummer.<blockquote>[!NOTE] Als u symbolen wilt elimineren uit alfabetten die niet ISO-conform zijn, moet de invoerparameter worden vertaald voordat deze wordt doorgegeven aan deze functie.</blockquote> | **ISOCredRef ("VEND-200002")** retourneert **"RF23VEND-200002"**. |
| CN\_GBT\_AdditionalDimensionID (tekenreeks, getal) | De opgegeven aanvullende financiële dimensie-id ophalen. In de parameter **string** worden dimensies vertegenwoordigd als id's die door komma's gescheiden zijn. De parameter **number** definieert de gewenste volgordecode van de gevraagde dimensie in de tekenreeks. | **CN\_GBT\_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH",3)** retourneert **"CC"**. |
| GetCurrentCompany () | Retourneert een tekstrepresentatie van de code van de rechtspersoon (bedrijf) waarbij een gebruiker momenteel is aangemeld. | **GETCURRENTCOMPANY ()** retourneert **USMF** voor een gebruiker die zich heeft aangemeld bij het bedrijf **Contoso Entertainment System USA** in Finance and Operations. |
| CH\_BANK\_MOD\_10 (cijfers) | Retourneer een crediteurverwijzing als een MOD10-expressie op basis van de cijfers van het opgegeven factuurnummer. | **CH\_BANK\_MOD\_10 ("VEND-200002")** retourneert **3**. |
| FA\_SUM (code vast activum, waardemodelcode, begindatum, einddatum) | Retourneert de voorbereide gegevenscontainer van de vaste-activabedragen voor de opgegeven periode. | **FA\_SUM ("COMP-000001", “Current”, Date1, Date2)** retourneert de voorbereide gegevenscontainer van het vaste activum **"COMP-000001"** met het waardemodel **"Current"** voor een periode van **Date1** tot **Date2**. |
| FA\_BALANCE (code vast activum, waardemodelcode, aangiftejaar, aangiftedatum) | Retourneert de voorbereide gegevenscontainer van het vaste-activasaldo. Het rapportjaar moet zijn opgegeven als een waarde van de opsomming **AssetYear** in Finance and Operations. | **FA\_SUM ("COMP-000001", “Current”, AxEnumAssetYear.ThisYear, SESSIONTODAY ())** retourneert de voorbereide gegevenscontainer met saldi voor het vaste activum **"COMP-000001"** met het waardemodel **"Current"** op de datum van de huidige Finance and Operations-sessie. |
| TABLENAME2ID (tekenreeks) | Retourneert een integer-representatie van een tabel-id voor de opgegeven tabelnaam. | **TABLENAME2ID ("Intrastat")** retourneert **1510**. |
| ISVALIDCHARACTERISO7064 (tekenreeks) | Retourneert de Booleaanse waarde **TRUE** wanneer de opgegeven tekenreeks staat voor een geldig internationaal bankrekeningnummer (IBAN). Anders de Booleaanse waarde **FALSE** retourneren. | **ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")** retourneert **TRUE**. **ISVALIDCHARACTERISO7064 ("AT61")** retourneert **FALSE**. |
| NUMSEQVALUE (getalreekscode, bereik, bereik-id) | De nieuw gegenereerde waarde van een getalreeks retourneren, op basis van de opgegeven getalreekscode, het bereik en de bereik-id. Het bereik moet worden opgegeven als een waarde van de opsomming **ERExpressionNumberSequenceScopeType** (**Gedeeld**, **Rechtspersoon** of **Bedrijf**). Geef voor het bereik **Gedeeld** een lege tekenreeks als de bereik-id op. Geef voor de bereiken **Bedrijf** en **Rechtspersoon** de bedrijfscode op als de bereik-id. Als u voor de bereiken **Bedrijf** en **Rechtspersoon** een lege tekenreeks opgeeft als de bereik-id, wordt de huidige bedrijfscode gebruikt. | U definieert de volgende gegevensbronnen in uw modeltoewijzing:<ul><li>**enumScope** (type **Dynamics 365 for Operations -opsomming**), die verwijst naar de opsomming **ERExpressionNumberSequenceScopeType**</li><li>**NumSeq** (type **Berekend veld**) die de expressie **NUMSEQVALUE ("Gene\_1" , enumScope.Company, "")** bevat</li></ul>Wanneer de gegevensbron **NumSeq** wordt aangeroepen, retourneert deze de nieuw gegenereerde waarde van de getalreeks **Gene\_1**, die is geconfigureerd voor het bedrijf dat de context levert waarin de ER-indeling wordt uitgevoerd. |
| NUMSEQVALUE (getalreekscode) | De nieuw gegenereerde waarde van een getalreeks retourneren op basis van de opgegeven getalreeks, het bereik **Bedrijf** en (als de bereik-id) de code van het bedrijf dat de context levert waarin de ER-indeling wordt uitgevoerd. | U definieert de volgende gegevensbron in uw modeltoewijzing: **NumSeq** (type **Berekend veld**). Deze gegevensbron bevat de expressie **NUMSEQVALUE ("Gene\_1")**. Wanneer de gegevensbron **NumSeq** wordt aangeroepen, retourneert deze de nieuw gegenereerde waarde van de getalreeks **Gene\_1**, die is geconfigureerd voor het bedrijf dat de context levert waarin de ER-indeling wordt uitgevoerd. |
| NUMSEQVALUE (getalreeksrecord-id) | De nieuw gegenereerde waarde van een getalreeks retourneren, op basis van de opgegeven getalreeksrecord-id. | U definieert de volgende gegevensbronnen in uw modeltoewijzing:<ul><li>**LedgerParms** (type **Tabel** type), dat verwijst naar de tabel LedgerParameters</li><li>**NumSeq** (type **Berekend veld** type), dat de expressie **NUMSEQVALUE (LedgerParameters.'numRefJournalNum()'.NumberSequenceId)** bevat</li></ul>Wanneer de gegevensbron **NumSeq** wordt aangeroepen, retourneert deze de nieuw gegenereerde waarde van de getalreeks die is geconfigureerd in de grootboekparameters voor het bedrijf dat de context levert waarin de ER-indeling wordt uitgevoerd. Deze getalreeks vormt een unieke identificatie van journalen en fungeert als batchnummer dat de transacties aan elkaar koppelt. |

### <a name="functions-list-extension"></a>Uitbreiding lijst met functies

MET ER kunt u de lijst met functies uitbreiden die in ER-expressies worden gebruikt. Hiervoor is enige mate van engineering vereist. Zie voor gedetailleerde informatie [De lijst met functies voor elektronische rapportage uitbreiden](general-electronic-reporting-formulas-list-extension.md).

## <a name="additional-resources"></a>Aanvullende resources

- [Overzicht van elektronische rapportage](general-electronic-reporting.md)
- [De lijst met functies voor elektronische rapportage (ER) uitbreiden](general-electronic-reporting-formulas-list-extension.md)
