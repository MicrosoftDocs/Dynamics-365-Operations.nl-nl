---
title: Formuleontwerper in elektronische rapportage
description: 'In dit onderwerp wordt beschreven hoe de formuleontwerper in elektronische rapportage (ER) wordt gebruikt. Wanneer u een indeling voor een specifiek elektronisch document in ER ontwerpt, kunt u Microsoft Excel-achtige formules voor gegevenstransformatie gebruiken om te voldoen aan de vereisten voor de afhandeling en opmaak van dat document. Verschillende typen functies worden ondersteund: tekst, datum en tijd, wiskundige logische, informatie, gegevenstypen en andere (business domein-specifieke functies).'
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: ac8d6c064ca826cc1c2fed07578ca9ce0c66ef66
ms.lasthandoff: 03/31/2017


---

# <a name="formula-designer-in-electronic-reporting"></a>Formuleontwerper in elektronische rapportage

In dit onderwerp wordt beschreven hoe de formuleontwerper in elektronische rapportage (ER) wordt gebruikt. Wanneer u een indeling voor een specifiek elektronisch document in ER ontwerpt, kunt u Microsoft Excel-achtige formules voor gegevenstransformatie gebruiken om te voldoen aan de vereisten voor de afhandeling en opmaak van dat document. Verschillende typen functies worden ondersteund: tekst, datum en tijd, wiskundige logische, informatie, gegevenstypen en andere (business domein-specifieke functies).

<a name="formula-designer-overview"></a>Overzicht van formuleontwerper
-------------------------

Elektronische rapportage (ER) ondersteunt de formuleontwerper. Daarom kunt u tijdens het ontwerpen expressies configureren die kunnen worden gebruikt voor de volgende taken in runtime:

-   Gegevens transformeren uit Microsoft Dynamics 365 for Operations-databases, die moeten worden ingevuld in een ER-gegevensmodel dat is bedoeld als gegevensbron voor ER-indelingen (filteren, groeperen, gegevenstypeconversie, enzovoort).
-   Gegevens opmaken die moeten worden verzonden naar een genererend elektronisch document in overeenstemming met de indeling en voorwaarden van de specifieke ER-indeling (in overeenstemming met aangevraagde taal of cultuur, codering, enzovoort).
-   Het proces beheren voor het maken van elektronische documenten (uitvoer van specifieke indelingselementen in-/uitschakelen afhankelijk van gegevensverwerking, het maken van documenten onderbreken, berichten voor eindgebruikers initiëren, enzovoort).

De pagina Formuleontwerper kan worden geopend wanneer u een van de volgende handelingen uitvoert:

-   De binding van gegevensbronartikelen aan gegevensmodelonderdelen.
-   De binding van gegevensbronartikelen aan indelingsonderdelen.
-   Het onderhoud van berekende velden als onderdeel van gegevensbronnen.
-   De definitie van zichtbaarheidvoorwaarden voor gebruikersinvoerparameters.
-   Het ontwerp van transformaties van de indeling.
-   De definitie van voorwaarden voor het inschakelen van de indelingsonderdelen.
-   De definitie van bestandsnamen voor de bestandsonderdelen van de indeling.
-   De definitie van de voorwaarden voor procescontrolevalidaties.
-   De definitie van de berichttekst voor procescontrolevalidaties.

## <a name="designing-er-formulas"></a>ER-formules ontwerpen
### <a name="data-binding"></a>Gegevensbinding

De ER-formuleontwerper kan worden gebruikt om een expressie te definiëren voor de transformatie van gegevens die worden ontvangen van gegevensbronnen, zodat de gegevens tijdens uitvoering in de gegevensconsument kunnen worden ingevoerd:

-   Vanuit Dynamics 365 for Operations-gegevensbronnen en uitvoeringsparameters naar een ER-gegevensmodel.
-   Vanuit een ER-gegevensmodel naar een ER-indeling.
-   Vanuit Dynamics 365 for Operations-gegevensbronnen en uitvoeringsparameters naar een ER-indeling.

De volgende afbeelding toont het ontwerp van een expressie van dit type. In dit voorbeeld retourneert de expressie de waarde van het veld **Intrastat.AmountMST** van de Dynamics 365 for Operations-tabel **Intrastat** nadat die waarde naar twee decimalen is afgerond. [![afbeelding expressie bindende](./media/picture-expression-binding.jpg)](./media/picture-expression-binding.jpg) de volgende afbeelding ziet u hoe een expressie van dit type kan worden gebruikt. In dit voorbeeld wordt het resultaat van de expressie ontworpen ingevuld het **Transaction.InvoicedAmount** onderdeel van de **btw-aangifte model** gegevensmodel. [![afbeelding-expressie-binding2](./media/picture-expression-binding2.jpg)](./media/picture-expression-binding2.jpg) tijdens de uitvoering, de formule ontworpen, **ronde (Intrastat.AmountMST, 2)**, moeten worden afgerond de waarde van de **AmountMST** veld voor elke record van de **Intrastat** tabel met twee decimalen en de afgeronde waarde aan te vullen de **Transaction.InvoicedAmount** onderdeel van de **btw-aangifte** gegevensmodel.

### <a name="data-formatting"></a>Gegevensnotatie

De ER-formuleontwerper kan worden gebruikt om een expressie te definiëren voor de opmaak van gegevens die worden ontvangen van gegevensbronnen, zodat de gegevens kunnen worden verzonden als onderdeel van het genererende elektronische document. Als u opmaak hebt die moet worden toegepast als een normale regel die opnieuw moet worden gebruikt voor een indeling, kunt u die opmaak één keer introduceren in een indelingsconfiguratie als een benoemde transformatie met een opmaakexpressie. Deze benoemde transformatie kan vervolgens worden gekoppeld aan vele indelingscomponenten waarvan de uitvoer volgens de gemaakte expressie moet worden opgemaakt. De volgende afbeelding toont het ontwerp van een transformatie van dit type. In dit voorbeeld neemt de transformatie **TrimmedString** inkomende gegevens van het gegevenstype **Tekenreeks** en worden spaties vooraan en achteraan verwijderd wanneer de tekenreekswaarde wordt geretourneerd. [![afbeelding-transformatie-ontwerp](./media/picture-transformation-design.jpg)](./media/picture-transformation-design.jpg) de volgende afbeelding ziet u hoe een transformatie van dit type kan worden gebruikt. In dit voorbeeld verwijzen verschillende indelingsonderdelen die tijdens uitvoering tekst als uitvoer naar het genererende elektronische document verzenden op naam naar de transformatie **TrimmedString**. [![afbeelding-transformatie-syntaxis](./media/picture-transformation-usage.jpg)](./media/picture-transformation-usage.jpg) als indeling onderdelen verwijst naar de ** TrimmedString ** transformatie (bijvoorbeeld de **partyName** onderdeel in het voorgaande voorbeeld) deze tekst als uitvoer verzendt naar het document genereren. De tekst bevat geen spaties vooraan en achteraan. Als u een opmaak hebt die afzonderlijk moet worden toegepast, kan deze opmaak als een afzonderlijke expressie van een binding van een specifieke indelingscomponent worden geïntroduceerd. De volgende afbeelding toont een expressie van dit type. In dit voorbeeld is het indelingsonderdel **partyType** gebonden aan de gegevensbron via een expressie waarmee inkomende gegevens vanuit het veld **Model.Company.RegistrationType** in de gegevensbron wordt geconverteerd naar tekst in hoofdletters en die tekst als uitvoer naar het elektronische document wordt verzonden. [![afbeelding bindende met formule](./media/picture-binding-with-formula.jpg)](./media/picture-binding-with-formula.jpg)

### <a name="process-flow-control"></a>Processtroombeheer

De ER-formuleontwerper kan worden gebruikt om expressies definiëren die de processtroom beheren voor het genereren van documenten. U kunt:

-   Definieer voorwaarden die bepalen wanneer het maken van een document moet worden gestopt.
-   Geef expressies op waarmee berichten voor eindgebruikers over gestopte processen of uitvoeringslogboekberichten over het voortzetten van het genereren van rapporten worden gemaakt.
-   Geef de bestandsnamen op van genererende documenten en beheer de voorwaarden voor het maken hiervan.

Elke regel van het processtroombeheer is ontworpen als afzonderlijke validatie. De volgende afbeelding toont een validatie van dit type. Hier volgt een uitleg van de configuratie in dit voorbeeld:

-   De validatie wordt geëvalueerd als het knooppunt **INSTAT** in het genererende XML-bestand wordt gemaakt.
-   Als de lijst met transacties leeg is, stopt de validatie het uitvoeringsproces en retourneert **FALSE**.
-   De validatie retourneert een foutbericht dat de tekst van label SYS70894 bevat in de voorkeurstaal van de gebruiker.

[![afbeelding validatie](./media/picture-validation.jpg)](./media/picture-validation.jpg) de Emergency Recovery Formuleontwerper kan ook worden gebruikt een bestandsnaam opgeven voor een genereren elektronisch document en het proces voor het maken van bestand controleren. De volgende afbeelding toont het ontwerp van een processtroombesturingselement van dit type. Hier volgt een uitleg van de configuratie in dit voorbeeld:

-   De lijst met records uit de gegevensbron **model.Intrastat** wordt verdeeld in batches die elk tot 1.000 records bevatten.
-   De uitvoer maakt een zipbestand dat een bestand in XML-indeling bevat voor elke batch die is gemaakt.
-   Een expressie retourneert een bestandsnaam voor genererende elektronische documenten door de bestandsnaam en bestandsextensie aaneen te schakelen. Voor de tweede en alle volgende batches bevat de bestandsnaam de batch-id als achtervoegsel.
-   Een expressie activeert (door **TRUE** te retourneren) het maken van een bestand voor batches die ten minste één record bevatten.

[![besturingselement van een afbeelding bestanden](./media/picture-file-control.jpg)](./media/picture-file-control.jpg)

### <a name="basic-syntax"></a>Basissyntaxis

ER-expressies kunnen een of alle van de volgende elementen bevatten:

-   Constanten
-   Operatoren
-   Verwijzingen
-   Paden
-   Functies

#### <a name="constants"></a>Constanten

U kunt tekst- en numerieke constanten (waarden die niet worden berekend) gebruiken bij het ontwerpen van expressies. Bijvoorbeeld de expressie ** waarde ('100') + 20 ** gebruikt de numerieke constante 20 en de tekenreeks '100' constante en de numerieke waarde **120**. De ER-formulierontwerper ondersteunt escapereeksen, wat betekent dat u de expressietekenreeks kunt opgeven die anders moet worden afgehandeld. De expressie **""Leo Tolstoy ""War and Peace"" Volume 1"** retourneert bijvoorbeeld de tekstreeks **Leo Tolstoy "War and Peace" Volume 1**.

#### <a name="operators"></a>Operatoren

De volgende tabel toont de rekenkundige operators die u kunt gebruiken om wiskundige basisbewerkingen uit te voeren, zoals optelling, aftrekking, deling en vermenigvuldiging.

| Operator | Betekenis              | Voorbeeld |
|----------|----------------------|---------|
| +        | Optelling             | 1+2     |
| -        | Aftrekkingsnegatie | 5-2 -1  |
| \*       | Vermenigvuldigen       | 7\*8    |
| /        | Afdeling             | 9/3     |

De volgende tabel toont de vergelijkingsoperators die worden ondersteund en die u kunt gebruiken om twee waarden te vergelijken.

| Operator | Betekenis                  | Voorbeeld    |
|----------|--------------------------|------------|
| =        | Gelijk                    | X=Y        |
| &gt;     | Groter dan             | X&gt;Y     |
| &lt;     | Kleiner dan                | X&lt;Y     |
| &gt;=    | Groter dan of gelijk aan | X&gt;=Y    |
| &lt;=    | Kleiner dan of gelijk aan    | X&lt;=Y    |
| &lt;&gt; | Niet gelijk aan             | X&lt;&gt;Y |

U kunt bovendien een en-teken (&) gebruiken als operator voor tekstaaneenschakeling om één of meer tekenreeksen in één eenheid tekst samen te voegen of aaneen te schakelen.

| Operator | Betekenis     | Voorbeeld                                        |
|----------|-------------|------------------------------------------------|
| &        | Samenvoegen | "Er is niets om af te drukken" & ": " & "geen records gevonden" |

#### <a name="operator-precedence"></a>Operatorprioriteit

De volgorde waarin de onderdelen van een samenstellingsexpressie worden geëvalueerd, is belangrijk. Bijvoorbeeld het resultaat van de expressie ** 1 + 4 / 2 ** verschilt, afhankelijk van of de bewerking toevoeging of de afdeling eerst wordt uitgevoerd. U kunt haakjes gebruiken om expliciet te definiëren hoe een expressie wordt geëvalueerd. Als u bijvoorbeeld wilt aangeven dat de optellingsbewerking eerst moet worden uitgevoerd, kunt u de voorafgaande expressie wijzigen in **(1 + 4) / 2**. Als de volgorde van bewerkingen die moeten worden uitgevoerd in een expressie, niet expliciet is gedefinieerd, wordt de volgorde gebaseerd op de standaardprioriteit die aan de ondersteunde operators is toegewezen. De volgende tabellen tonen de operators en de prioriteit die aan elk is toegewezen. Operators met een hogere prioriteit (bijvoorbeeld 7) worden eerder geëvalueerd dan operators met een lagere prioriteit (bijvoorbeeld 1).

| Prioriteit | Operatoren      | Syntaxis                                                   |
|------------|----------------|----------------------------------------------------------|
| 7          | Groepering       | ( … )                                                    |
| 6          | Toegankelijkheid voor leden  | … . …                                                    |
| 5          | Functieaanroep  | … ( … )                                                  |
| 4          | Vermenigvuldigen | … \* … … / …                                             |
| 3          | Additief       | … + … … - …                                              |
| 2          | Vergelijking     | … &lt; … … &lt;= … … =&gt; … … &gt; … … = … … &lt;&gt; … |
| 1          | Scheidingsteken     | … , …                                                    |

Operators op dezelfde regel hebben dezelfde prioriteit. Als een expressie meerdere van deze operators bevat, wordt de expressie van links naar rechts geëvalueerd. Bijvoorbeeld de expressie **1 + 6 / 2 \*3 &gt;5** retourneert **true**. We raden aan haakjes te gebruiken om de gewenste evaluatievolgorde voor expressies expliciet aan te geven, zodat de expressies gemakkelijker te lezen en onderhouden zijn.

#### <a name="references"></a>Verwijzingen

Alle gegevensbronnen van het huidige ER-onderdeel (een model of een indeling) die tijdens het ontwerp van een expressie beschikbaar zijn, kunnen als benoemde verwijzingen worden gebruikt. Het huidige ER-gegevensmodel bevat bijvoorbeeld de gegevensbron **ReportingDate** die een waarde van het gegevenstype **DATETIME** retourneert. Om juist die waarde in het document genereren, kunt u verwijzen naar de gegevensbron in de expressie als volgt: **DATETIMEFORMAT (ReportingDate, 'dd-MM-jjjj')** alle tekens in de naam van een gegevensbron verwijzen naar die staan voor een brief van het alfabet niet moeten worden voorafgegaan door een enkel aanhalingsteken ('). Als de naam van een gegevensbron verwijzen naar ten minste één symbool dat niet een letter van het alfabet (bijvoorbeeld leestekens of andere geschreven symbolen) bevat, moet u de naam tussen enkele aanhalingstekens staan. Hieronder vindt u enkele voorbeelden:

-   In een ER-expressie moet als volgt naar de gegevensbron **Datum en tijd van vandaag** worden verwezen: **'Datum en tijd van vandaag'**
-   Naar de methode **name()** van de gegevensbron **Klanten** moet in een ER-expressie als volgt worden verwezen: **Customers.'name()'**

#### <a name="path"></a>Pad

Wanneer een expressie naar een gestructureerde gegevensbron verwijst, kunt u de paddefinitie gebruiken om een specifiek primitief element van deze gegevensbron te selecteren. Een puntteken (.) wordt gebruikt om afzonderlijke individuele elementen van een gestructureerde gegevensbron te scheiden. Het huidige ER-gegevensmodel bevat bijvoorbeeld de gegevensbron **InvoiceTransactions** die een lijst met records retourneert. De recordstructuur** InvoiceTransactions** bevat de velden **AmountDebit** en **AmountCredit**, die numerieke waarden retourneren. U kunt daarom de volgende expressie ontwerpen om het gefactureerde bedrag te berekenen: **InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit**

#### <a name="functions"></a>Functies

Het volgende onderdeel beschrijft de taken die kunnen worden gebruikt in ER-expressies. Alle gegevensbronnen van de expressiecontext (het huidige ER-gegevensmodel of de huidige ER-indeling) en ook constanten kunnen als parameters worden gebruikt van functieaanroepen volgens de lijst met argumenten voor functieaanroepen. Het huidige ER-gegevensmodel bevat bijvoorbeeld de gegevensbron **InvoiceTransactions** die een lijst met records retourneert. De recordstructuur** InvoiceTransactions** bevat de velden **AmountDebit** en **AmountCredit**, die numerieke waarden retourneren. Voor het berekenen van het gefactureerde bedrag kunt u daarom de volgende expressie ontwerpen die de ingebouwde ER-afrondingsfunctie gebruikt: **ROUND (InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit, 2)**

## <a name="supported-functions"></a>Ondersteunde functies
De volgende tabellen beschrijven de functies voor gegevensmanipulatie die u kunt gebruiken om ER-gegevensmodellen en ER-rapporten te ontwerpen. De lijst van functies is niet vast en kan door ontwikkelaars worden uitgebreid. Open het functievenster in de ER-formuleontwerper om de lijst van functies te bekijken die u kunt gebruiken.

### <a name="date-and-time-functions"></a>Datum- en tijdfuncties

| Functie                                   | Beschrijving                                                                                                                                                                                                                                                                                                                                                      | Voorbeeld                                                                                                                                                                                                                                                                                               |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ADDDAYS (datum/tijd, dagen)                   | Voeg het opgegeven aantal dagen aan de opgegeven datum-/tijdwaarde toe.                                                                                                                                                                                                                                                                                                | **ADDDAYS (NOW(), 7)** retourneert de datum en tijd van zeven dagen in de toekomst.                                                                                                                                                                                                                            |
| DATETODATETIME (datum)                      | Zet de opgegeven datumwaarde om naar een datum-/tijdwaarde.                                                                                                                                                                                                                                                                                                            | **DATETODATETIME (CompInfo. ' getCurrentDate()')** retourneert de huidige Dynamics 365 for Operations sessiedatum, 24-12/2015 als **12/24/2015 12:00:00 AM**. In dit voorbeeld is **CompInfo** een ER-gegevensbron van het type **Dynamics 365 for Operations/Table** die naar de tabel CompanyInfo verwijst. |
| NOW ()                                     | Retourneer de huidige datum en tijd van de Dynamics 365 for Operations-toepassingsserver als een datum-/tijdwaarde.                                                                                                                                                                                                                                                             |                                                                                                                                                                                                                                                                                                       |
| TODAY ()                                   | Retourneer de huidige datum van de Dynamics 365 for Operations-toepassingsserver als een datumwaarde.                                                                                                                                                                                                                                                                          |                                                                                                                                                                                                                                                                                                       |
| NULLDATE ()                                | Retourneer een **null**-datumwaarde.                                                                                                                                                                                                                                                                                                                                    |                                                                                                                                                                                                                                                                                                       |
| NULLDATETIME ()                            | Retourneer een **null**-datum-/tijdwaarde.                                                                                                                                                                                                                                                                                                                                |                                                                                                                                                                                                                                                                                                       |
| DATETIMEFORMAT (datum/tijd, indeling)          | Converteer de opgegeven datum-/tijdwaarde naar een tekenreeks in de opgegeven indeling. (Zie voor informatie over de ondersteunde indelingen [standaard](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) en [aangepast](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx).)                                                                        | **DATETIMEFORMAT (NOW(), "dd-MM-yyyy")** retourneert de huidige datum van de Dynamics 365 for Operations-toepassingsserver, 12/24/2015, als **"24-12-2015"** volgens de opgegeven aangepaste indeling.                                                                                                          |
| DATETIMEFORMAT (datum/tijd, indeling, cultuur) | Converteer de opgegeven datum-/tijdwaarde naar een tekenreeks in de opgegeven indeling en [cultuur](https://msdn.microsoft.com/en-us/goglobal/bb896001.aspx). (Zie voor informatie over de ondersteunde indelingen [standaard](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) en [aangepast](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx)). | **DATETIMEFORMAT (NOW(), "d", "de")** retourneert de huidige datum van de Dynamics 365 for Operations-toepassingsserver, 12/24/2015, als **"24.12.2015"** volgens de geselecteerde Duitse cultuur.                                                                                                             |
| SESSIONTODAY ()                            | Retourneer de datum van de huidige Dynamics 365 for Operations-sessie als een datumwaarde.                                                                                                                                                                                                                                                                                      |                                                                                                                                                                                                                                                                                                       |
| SESSIONNOW ()                              | Retourneer de datum en tijd van de huidige Dynamics 365 for Operations-sessie als een datum-/tijdwaarde.                                                                                                                                                                                                                                                                         |                                                                                                                                                                                                                                                                                                       |
| DATEFORMAT (datum, indeling)                  | Retourneert een tekenreeksvoorstelling van de datum met de opgegeven indeling.                                                                                                                                                                                                                                                                                                    | **DATEFORMAT (SESSIONTODAY (), "dd-MM-yyyy")** retourneert de huidige datum van de Dynamics 365 for Operations-sessie 12/24/2015 als “**24-12-2015**” volgens de opgegeven aangepast indeling.                                                                                                                      |
| DATEFORMAT (datum, indeling, cultuur)         | Converteer de opgegeven datumwaarde naar een tekenreeks in de opgegeven indeling en [cultuur](https://msdn.microsoft.com/en-us/goglobal/bb896001.aspx). (Zie voor informatie over de ondersteunde indelingen [standaard](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) en [aangepast](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx)).     | **DATETIMEFORMAT (SESSIONNOW (), "d", "de")** retourneert de huidige datum van de Dynamics 365 for Operations-sessie, 12/24/2015, als **"24.12.2015"** volgens de geselecteerde Duitse cultuur.                                                                                                                       |

### <a name="list-functions"></a>Lijstfuncties

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Functie</th>
<th>Omschrijving</th>
<th>Voorbeeld</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>SPLIT (invoer, lengte)</td>
<td>Splits de opgegeven invoertekenreeks in subreeksen, waarvan elk de opgegeven lengte heeft. Retourneer het resultaat als een nieuwe lijst.</td>
<td><strong>SPLITSEN (&quot;abcd&quot;, 3)</strong> resulteert in een nieuwe lijst die bestaat uit twee records met een <strong>tekenreeks</strong> veld. Bevat de tekst van het veld in de eerste record <strong>&quot;abc&quot;</strong>, en bevat de tekst van het veld in de tweede record <strong>&quot;d&quot;</strong>.</td>
</tr>
<tr class="even">
<td>SPLITLIST (lijst, aantal)</td>
<td>Splits de opgegeven lijst in batches waarvan elk het opgegeven aantal records bevat. Retourneer het resultaat als een nieuwe lijst batches die de volgende elementen bevatten:
<ul>
<li>Batches als normale lijsten (onderdeel <strong>Waarde </strong>)</li>
<li>Het huidige batchaantal (onderdeel <strong>BatchNumber </strong>)</li>
</ul></td>
<td>In het volgende voorbeeld wordt de gegevensbron <strong>Regels</strong> gemaakt als een recordlijst van drie records die wordt verdeeld in batches, waarvan elk maximaal twee records bevat. <a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>Hier wordt de indeling ontworpen opmaak waarin bindingen met de <strong>regels</strong> gegevensbron zijn gemaakt voor het genereren van uitvoer in XML-indeling waarin de afzonderlijke knooppunten voor elke batch en de records in deze. <a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>De volgende is het resultaat van het uitvoeren van de indeling ontworpen. <a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a></td>
</tr>
<tr class="odd">
<td>LIST (record 1 [, record 2, ...])</td>
<td>Retourneer een nieuwe lijst die wordt gemaakt van de opgegeven argumenten.</td>
<td><strong>LIST (model.MainData, model.OtherData)</strong> retourneert een lege record, waarbij de lijst met velden alle velden bevat van de recordlijsten <strong>MainData</strong> en <strong>OtherData</strong>.</td>
</tr>
<tr class="even">
<td>LISTJOIN (lijst 1, lijst 2, ...)</td>
<td>Retourneer een gecombineerde lijst die wordt gemaakt van lijsten van opgegeven argumenten.</td>
<td><strong>LISTJOIN (splitsen (&quot;abc&quot;, 1), splitsen (&quot;def&quot;, 1))</strong> resulteert in de lijst met zes records wanneer een veld van de <strong>tekenreeks</strong> gegevenstype bevat één letter.</td>
</tr>
<tr class="odd">
<td>ISEMPTY (lijst)</td>
<td>Retourneer <strong>TRUE</strong> als de opgegeven lijst geen elementen bevat. Retourneer anders <strong>FALSE</strong>.</td>
<td></td>
</tr>
<tr class="even">
<td>EMPTYLIST (lijst)</td>
<td>Retourneer een lege lijst door de opgegeven lijst te gebruiken als een bron voor de lijststructuur.</td>
<td><strong>EMPTYLIST (splitsen (&quot;abc&quot;, 1))</strong> resulteert in een nieuwe lege lijst met dezelfde structuur als de lijst die wordt geretourneerd door <strong>splitsen</strong> functie.</td>
</tr>
<tr class="odd">
<td>FIRST (lijst)</td>
<td>Retourneer de eerste record van de opgegeven lijst, als die record niet leeg is. Anders treedt een uitzondering op.</td>
<td></td>
</tr>
<tr class="even">
<td>FIRSTORNULL (lijst)</td>
<td>Retourneer de eerste record van de opgegeven lijst, als die record niet leeg is. Retourneer anders een <strong>null</strong>-record.</td>
<td></td>
</tr>
<tr class="odd">
<td>LISTOFFIRSTITEM (lijst)</td>
<td>Retourneer een lijst die alleen het eerste item uit de opgegeven lijst bevat.</td>
<td></td>
</tr>
<tr class="even">
<td>ALLITEMS (pad)</td>
<td>Retourneer een nieuwe afgevlakte lijst die alle items vertegenwoordigt die overeenkomen met het opgegeven pad. Het pad moet worden gedefinieerd als een geldig gegevensbronpad naar een gegevensbronelement van een gegevenstype van de recordlijst. Het pad naar gegevenselementen als tekenreeks, datum enzovoort moet een fout opleveren bij het ontwerpen in de ER Expression Builder.</td>
<td>Als u <strong>splitsen (&quot;abcdef&quot;, 2)</strong> als een gegevensbron (DS), <strong>TELLING (ALLITEMS (Active Directory. Waarde))</strong> retourneert <strong>3</strong>.</td>
</tr>
<tr class="odd">
<td>ORDERBY (lijst [, expressie 1, expressie 2, …])</td>
<td>Retourneer de opgegeven lijst, die is gesorteerd op basis van de opgegeven argumenten die kunnen worden gedefinieerd als expressies.</td>
<td>Wanneer <strong>Leverancier </strong> als een ER-gegevensbron wordt geconfigureerd die naar de tabel VendTable verwijst, retourneert <strong>ORDERBY (Leveranciers,Leverancier.'naam() ')</strong> de lijst met leveranciers die in oplopende volgorde op naam is gesorteerd.</td>
</tr>
<tr class="even">
<td>REVERSE (lijst)</td>
<td>Retourneer de opgegeven lijst in omgekeerde sorteervolgorde.</td>
<td>Wanneer <strong>Leverancier </strong> als een ER-gegevensbron wordt geconfigureerd die naar de tabel VendTable verwijst, retourneert <strong>REVERSE (ORDERBY (Leveranciers,Leverancier.'naam()')) )</strong> de lijst met leveranciers die in aflopende volgorde op naam is gesorteerd.</td>
</tr>
<tr class="odd">
<td>WHERE (lijst, voorwaarde)</td>
<td>Retourneer de opgegeven lijst die is gefilterd op basis van de opgegeven voorwaarde. In tegenstelling tot de functie <strong>FILTER</strong> wordt de opgegeven voorwaarde op de lijst in het geheugen toegepast.</td>
<td>Wanneer <strong>leverancier</strong> is geconfigureerd als een Emergency Recovery-gegevensbron die naar de tabel VendTable verwijst, <strong>waar (leveranciers, Vendors.VendGroup = &quot;40&quot;)</strong> resulteert in de lijst met leveranciers die tot de leveranciersgroep 40 behoren.</td>
</tr>
<tr class="even">
<td>ENUMERATE (lijst)</td>
<td>Retourneer een nieuwe lijst die bestaat uit opgesomde records van de opgegeven lijst en die de volgende elementen beschikbaar maakt:
<ul>
<li>Opgegeven lijstrecords als normale lijsten (component <strong>Waarde </strong>)</li>
<li>De huidige recordindex (onderdeel <strong>Nummer</strong>)</li>
</ul></td>
<td>In het volgende voorbeeld wordt de gegevensbron <strong>Genummerd</strong> gemaakt als een genummerde lijst leveranciersrecords van de gegevensbron <strong>Leveranciers</strong> die verwijst naar de tabel <strong>VendTable</strong>. <a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a>Hier wordt de indeling waarin de gegevensbindingen voor het genereren van uitvoer in XML-indeling waarin individuele leveranciers als opgesomde knooppunten worden gemaakt. <a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a>Dit is het resultaat van het uitvoeren van de indeling ontworpen. <a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a></td>
</tr>
<tr class="odd">
<td>COUNT (lijst)</td>
<td>Retourneer het aantal records in de opgegeven lijst, als de lijst niet leeg is. Retourneer anders <strong>0</strong> (nul).</td>
<td><strong>TELLING (splitsen (&quot;abcd&quot;, 3))</strong> retourneert <strong>2</strong>, omdat de <strong>splitsen</strong> functie maakt een lijst die uit twee records bestaat.</td>
</tr>
<tr class="even">
<td>LISTOFFIELDS (pad)</td>
<td>Retourneert een lijst met records die is gemaakt op basis van een argument van een van de volgende:
<ul>
<li>Modelopsomming</li>
<li>Opsomming van indelingen</li>
<li>Container</li>
</ul>
De gemaakte lijst bestat uit records met de volgende velden:
<ul>
<li>Naam</li>
<li>Etiket</li>
<li>Omschrijving</li>
</ul>
De velden Label en Omschrijving retourneren tijdens de uitvoering waarden op basis van de taalinstellingen van de indeling.</td>
<td>Het volgende voorbeeld toont de opsomming die in een gegevensmodel wordt geïntroduceerd. <a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="GER LISTOFFIELDS function - model enumeration" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a>Het volgende voorbeeld ziet:
<ul>
<li>Modelopsomming die in een rapport wordt ingevoegd als gegevensbron.</li>
<li>ER-expressie die is ontworpen om modelopsomming als parameter voor deze functie te gebruiken.</li>
<li>Gegevensbron van het type recordlijst die wordt ingevoegd in een rapport met de gemaakte ER-expressie.</li>
</ul><ph id="t1">
< een href="./media/ger-listoffields-function-in-format-expression.png" ></ph><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="GER LISTOFFIELDS function - in format expression" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a> in het volgende voorbeeld ziet u de Emergency Recovery-indeling-elementen die afhankelijk zijn van de gegevensbron van het type opnemen lijst die is gemaakt met de functie LISTOFFIELDS. <a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="GER LISTOFFIELDS function - format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a>Dit is het resultaat van de uitvoering ontworpen opmaak. <a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="GER LISTOFFIELDS function - format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a><strong>opmerking:</strong> vertaalde tekst voor labels en omschrijvingen voor Emergency Recovery indeling uitvoer overeenkomstig de taalinstellingen die is geconfigureerd voor het bovenliggende bestand en elementen op map wordt gevuld.</td>
</tr>
<tr class="odd">
<td>STRINGJOIN (lijst, veldnaam, scheidingsteken)</td>
<td>Retourneert de tekenreeks van samengevoegde waarden van een veld uit een lijst, van elkaar gescheiden met een geselecteerd scheidingsteken.</td>
<td>Als u SPLIT(“abc” , 1) hebt ingevoerd als een gegevensbron DS, wordt door expressie STRINGJOIN (DS, DS.Value, “:”) “a:b:c” geretourneerd</td>
</tr>
<tr class="even">
<td>SPLITLISTBYLIMIT (lijst, limietwaarde, limietbron)</td>
<td>Splitst de gedefinieerde lijst in een nieuwe lijst met sublijsten en retourneert het resultaat in de inhoud van de recordlijst. De grenswaardeparameter geeft de waarde van de limiet om de lijst van herkomst te splitsen. De parameter voor de limietbron geeft de stap aan waarmee de totale som wordt verhoogd. De limiet wordt niet toegepast op één artikel van de gedefinieerde lijst wanneer de limietbron de gedefinieerde limiet overschrijden.</td>
<td>In het volgende voorbeeld wordt de voorbeeldindeling weergegeven met gegevensbronnen. <a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="GER SPLITLISTBYLIMIT - format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a><a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="GER SPLITLISTBYLIMIT - datasources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a>Dit is het resultaat indeling uitvoeren waarin de platte lijst met basisproducten. <a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="GER SPLITLISTBYLIMIT - output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a>In het volgende voorbeeld ziet u dezelfde indeling die is gecorrigeerd om de lijst met basisproducten in batches worden weergegeven wanneer een partij grondstoffen met het totale gewicht dat mag niet hoger zijn dan de limiet van 9 moet bevatten. <a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="GER SPLITLISTBYLIMIT - format 1" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a><a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="GER SPLITLISTBYLIMIT - datasources 1" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a>Dit is het resultaat van de uitvoering van de aangepaste indeling. <a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="GER SPLITLISTBYLIMIT - output 1" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a><strong>opmerking:</strong> de limiet wordt niet toegepast op het laatste item van de oorsprong lijst omdat de waarde (11) van de limiet bron (gewicht) groter is dan de ingestelde limiet (9). Gebruik de functie <strong>WAAR</strong> of de expressie <strong>Ingeschakeld</strong> van het bijbehorende indelingselement om de sublijsten te negeren (overslaan) tijdens het genereren van het rapport (indien nodig).</td>
</tr>
<tr class="odd">
<td>FILTER (lijst, voorwaarde)</td>
<td>Retourneert de gedefinieerde lijst die is gefilterd voor de opgegeven voorwaarde door de query te wijzigen. In tegenstelling tot de functie <strong>WAAR</strong>, wordt de opgegeven voorwaarde toegepast op het databaseniveau op een willekeurige ER-gegevensbron van het type Tabelrecords.</td>
<td>FILTER (leveranciers, Vendors.VendGroup = &quot;40&quot;) resulteert in de lijst met alleen de leveranciers die behoren tot de leveranciers-groep '40' wanneer <strong>leverancier</strong> is geconfigureerd als Emergency Recovery-gegevensbron verwijzen naar de <strong>VendTable</strong> tabel</td>
</tr>
</tbody>
</table>

### <a name="logical-functions"></a>Logische functies

| Functie                                                                                | Omschrijving                                                                                                                                                                                                                                                                     | Voorbeeld                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AANVRAAG (expressie, optie 1, leiden tot 1 \[, optie 2, hetgeen leidt tot 2\] ... \[, standaard resultaat\]) | Evalueer de opgegeven expressiewaarde tegen de opgegeven alternatieve opties. Retourneer het resultaat van de optie die gelijk is aan de waarde van de expressie. Retourneer anders het optioneel ingevoerde standaardresultaat (de laatste parameter die niet door een optie wordt voorafgegaan). | **CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")** retourneert de tekenreeks **"WINTER"** wanneer de datum van de huidige Dynamics 365 for Operations-sessie tussen oktober en december is. Anders wordt een lege tekenreeks geretourneerd. |
| IF (voorwaarde, waarde 1, waarde 2)                                                        | Retourneer de opgegeven waarde 1 wanneer aan de gegeven voorwaarde is voldaan. Anders retourwaarde 2. Als de waarde 1 en de waarde 2 records of recordlijsten, heeft het resultaat alleen de velden die in beide lijsten voorkomen.                                                                     | **IF (1=2, "aan voorwaarde is voldaan", "aan voorwaarde is niet voldaan")** retourneert de tekenreeks ** "aan voorwaarde is niet voldaan"**.                                                                                                                                                      |
| NOT (voorwaarde)                                                                         | Retourneer de omgekeerde logische waarde van de opgegeven voorwaarde.                                                                                                                                                                                                                   | **NOT (WAAR)** retourneert **FALSE**.                                                                                                                                                                                                                            |
| EN (1-voorwaarde\[, voorwaarde 2;... \])                                                 | Retourneer **TRUE** als *alle * opgegeven voorwaarden waar zijn. Retourneer anders **FALSE**.                                                                                                                                                                                            | **AND (1=1, "a"="a")** retourneert **TRUE**. **AND (1=2, "a"="a")** retourneert **FALSE**.                                                                                                                                                                           |
| OF (1-voorwaarde\[, voorwaarde 2;... \])                                                  | Retourneer **FALSE** als *alle * opgegeven voorwaarden onwaar zijn. Retourneer **TRUE** als *een van de* opgegeven voorwaarden waar is.                                                                                                                                                                 | **OR (1=2, "a"="a")** retourneert **TRUE**.                                                                                                                                                                                                                      |

### <a name="mathematical-functions"></a>Wiskundige functies

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Functie</th>
<th>Beschrijving</th>
<th>Voorbeeld</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ABS (getal)</td>
<td>Retourneert de absolute waarde van het opgegeven getal (het getal zonder het teken ervan).</td>
<td><strong>ABS (-1)</strong> retourneert <strong>1</strong>.</td>
</tr>
<tr class="even">
<td>POWER (aantal, macht)</td>
<td>Retourneert het resultaat van het verheffen van het opgegeven positieve getal naar de opgegeven macht.</td>
<td><strong>POWER (10, 2)</strong> retourneert <strong>100</strong>.</td>
</tr>
<tr class="odd">
<td>NUMBERVALUE (tekenreeks, decimaal scheidingsteken, scheidingsteken groep komma)</td>
<td>Converteert de opgegeven tekenreeks naar een getal. Het opgegeven symbool wordt gebruikt om het hele getal en de fractiedelen van een decimaal getal te scheiden, en het opgegeven scheidingsteken voor duizendtallen wordt ook gebruikt.</td>
<td><strong>NUMBERVALUE (&quot;1 234,56&quot;, &quot;,&quot;, &quot;&quot;)</strong> retourneert de waarde <strong>1234,56</strong>.</td>
</tr>
<tr class="even">
<td>VALUE (tekenreeks)</td>
<td>Converteert de opgegeven tekenreeks naar een getal. De komma's en punttekens (.) worden beschouwd als decimale scheidingstekens en er wordt een koppelteken (-) vooraan gebruikt als minteken. Er treedt een uitzondering op als andere niet-numerieke tekens worden aangetroffen in de opgegeven tekenreeks.</td>
<td><strong>WAARDE (&quot;1 234,56&quot;)</strong> een uitzondering.</td>
</tr>
<tr class="odd">
<td>ROUND (getal, decimalen)</td>
<td>Retourneer het opgegeven getal, dat wordt afgerond naar het opgegeven aantal decimalen:
<ul>
<li>Als de opgegeven decimale waarde meer dan 0 (nul) is, wordt het opgegeven getal afgerond naar het opgegeven aantal decimalen.</li>
<li>Als de opgegeven decimale waarde 0 (nul) is, wordt het opgegeven getal afgerond naar het dichtstbijzijnde hele getal.</li>
<li>Als de opgegeven decimale waarde minder dan 0 (nul) is, wordt het opgegeven getal links van de decimale komma afgerond.</li>
</ul></td>
<td><strong>ROUND (1200,767, 2)</strong> rondt af naar twee decimalen en retourneert <strong>1200,77</strong>. <strong>ROUND (1200,767, -3)</strong> rondt af naar het dichtstbijzijnde veelvoud van 1.000 en retourneert <strong>1000</strong>.</td>
</tr>
<tr class="even">
<td>ROUNDDOWN (getal, decimalen)</td>
<td>Retourneer het opgegeven aantal, dat naar beneden wordt afgerond (naar nul) naar het opgegeven aantal decimalen. <strong>Opmerking:</strong> deze functie werkt als <strong>ROUND</strong>, maar het rondt altijd het opgegeven getal naar beneden af.</td>
<td><strong>ROUNDDOWN (1200,767, 2)</strong> rondt naar beneden af naar twee decimalen en retourneert <strong>1200,76</strong>. <strong>ROUNDDOWN (1700,767, -3)</strong> rondt naar beneden af naar het dichtstbijzijnde veelvoud van 1.000 en retourneert <strong>1000</strong>.</td>
</tr>
<tr class="odd">
<td>ROUNDUP (getal, decimalen)</td>
<td>Retourneer het opgegeven aantal, dat naar boven wordt afgerond (weg van nul) naar het opgegeven aantal decimalen. <strong>Opmerking:</strong> deze functie werkt als <strong>ROUND</strong>, maar het rondt altijd het opgegeven getal naar boven af.</td>
<td><strong>ROUNDUP (1200,763, 2)</strong> rondt naar boven af naar twee decimalen en retourneert <strong>1200,77</strong>. <strong>ROUNDUP (1200,767, -3)</strong> rondt naar boven af naar het dichtstbijzijnde veelvoud van 1.000 en retourneert <strong>2000</strong>.</td>
</tr>
</tbody>
</table>

### <a name="record-functions"></a>Registratiefuncties

| Functie             | Beschrijving                                                                                                                                                                                                                                     | Voorbeeld                                                                                                                                             |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| NULLCONTAINER (lijst) | Retourneer een **null**-record met dezelfde structuur als de opgegeven recordlijst of record. **Opmerking: **deze functie is verouderd. Gebruik in plaats daarvan **EMPTYRECORD**.                                                                                  | **NULLCONTAINER (SPLIT ("abc", 1))** retourneert een nieuwe lege record die dezelfde structuur heeft als de lijst die wordt geretourneerd door de functie **SPLIT**. |
| EMPTYRECORD (record) | Retourneer een **null**-record met dezelfde structuur als de opgegeven recordlijst of record. **opmerking:** A **null** record is een record waarin alle velden een lege waarde hebben (**0**\[nul\] voor getallen, een lege tekenreeks voor tekenreeksen, enzovoort). | **EMPTYRECORD (SPLIT ("abc", 1))** retourneert een nieuwe lege record die dezelfde structuur heeft als de lijst die wordt geretourneerd door de functie **SPLIT**.   |

### <a name="text-functions"></a>Tekstfuncties

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Functie</th>
<th>Beschrijving</th>
<th>Voorbeeld</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>UPPER (tekenreeks)</td>
<td>Retourneer de opgegeven tekenreeks, die wordt geconverteerd naar hoofdletters.</td>
<td><strong>BOVENSTE (&quot;voorbeeld&quot;)</strong> retourneert <strong>&quot;voorbeeld&quot;</strong>.</td>
</tr>
<tr class="even">
<td>LOWER (tekenreeks)</td>
<td>Retourneer de opgegeven tekenreeks, die wordt geconverteerd naar kleine letters.</td>
<td><strong>ONDERSTE (&quot;voorbeeld&quot;)</strong> retourneert <strong>&quot;voorbeeld&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>LEFT (tekenreeks, aantal tekens)</td>
<td>Retourneer het opgegeven aantal tekens vanaf het begin van de opgegeven tekenreeks.</td>
<td><strong>LINKS (&quot;voorbeeld&quot;, 3)</strong> retourneert <strong>&quot;Sam&quot;</strong>.</td>
</tr>
<tr class="even">
<td>RIGHT (tekenreeks, aantal tekens)</td>
<td>Retourneer het opgegeven aantal tekens vanaf het eind van de opgegeven tekenreeks.</td>
<td><strong>RECHTS (&quot;voorbeeld&quot;, 3)</strong> retourneert <strong>&quot;meerdere&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>MID (tekenreeks, beginpositie, aantal tekens)</td>
<td>Retourneer het opgegeven aantal tekens van de opgegeven tekenreeks, vanaf de opgegeven positie.</td>
<td><strong>MID (&quot;voorbeeld&quot;, 2, 3)</strong> retourneert <strong>&quot;amp&quot;</strong>.</td>
</tr>
<tr class="even">
<td>LEN (tekenreeks)</td>
<td>Retourneer het aantal tekens in de opgegeven tekenreeks.</td>
<td><strong>LENGTE (&quot;voorbeeld&quot;)</strong> retourneert <strong>6</strong>.</td>
</tr>
<tr class="odd">
<td>CHAR (getal)</td>
<td>Retourneer de tekenreeks waarnaar wordt verwezen door het opgegeven Unicode-getal.</td>
<td><strong>TEKENS (255)</strong> retourneert <strong>&quot;ÿ&quot;</strong>. <strong>Opmerking:</strong> De geretourneerde tekenreeks is afhankelijk van de codering die in het bovenliggende FILE-indelingelement is geselecteerd. U vindt de lijst met ondersteunde coderingen in het onderwerp <a href="https://msdn.microsoft.com/en-us/library/system.text.encoding(v=vs.110).aspx">Codering klasse</a>.</td>
</tr>
<tr class="even">
<td>CONCATENATE (tekenreeks 1 [, tekenreeks 2, …])</td>
<td>Retourneer alle opgegeven tekenreeksen, die zijn samengevoegd in één tekenreeks.</td>
<td><strong>SAMENVOEGEN (&quot;abc&quot;, &quot;def&quot;)</strong> retourneert <strong>&quot;abcdef&quot;</strong>. <strong>opmerking:</strong> de expressie <strong>&quot;abc&quot;&amp;&quot;def&quot;</strong> retourneert ook <strong>&quot;abcdef&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>TRANSLATE (tekenreeks, patroon, vervanging)</td>
<td>Retourneer de opgegeven tekenreeks, waarin alle gevonden tekens in de opgegeven patroontekenreeks worden vervangen door de tekens op de bijbehorende positie van de opgegeven vervangingstekenreeks.</td>
<td><strong>VERTALEN (&quot;abcdef&quot;, &quot;cd&quot;, &quot;GH&quot;)</strong> vervangt het patroon <strong>&quot;cd&quot;</strong> met de tekenreeks <strong>&quot;GH&quot;</strong> en retourneert <strong>&quot;abGHef&quot;</strong>.</td>
</tr>
<tr class="even">
<td>REPLACE (tekenreeks, patroon, vervanging, normale-expressiemarkering)</td>
<td>Wanneer de opgegeven normale-expressiemarkering <strong>waar</strong> is, de opgegeven tekenreeks retourneren, die wordt gewijzigd door de normale expressie toe te passen die als patroonargument voor deze functie wordt opgegeven. Deze expressie wordt gebruikt om tekens te zoeken die moeten worden vervangen. Tekens van het opgegeven vervangingsargument worden gebruikt om tekens te vervangen die zijn gevonden. Wanneer de opgegeven normale-expressiemarkering <strong>onwaar</strong> is, gedraagt deze functie zich als <strong>TRANSLATE</strong>.</td>
<td>  <strong>VERVANGEN (&quot;+1 923 456 4971&quot;, &quot;[^ 0-9]&quot;, &quot;&quot;, true)</strong> van toepassing is een reguliere expressie die wordt verwijderd van alle niet-numerieke symbolen en retourneert <strong>&quot;19234564971&quot;</strong>. <strong>VERVANGEN (&quot;abcdef&quot;, &quot;cd&quot;, &quot;GH&quot;, false)</strong> vervangt het patroon <strong>&quot;cd&quot;</strong> met de tekenreeks <strong>&quot;GH&quot;</strong> en retourneert <strong>&quot;abGHef&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>TEXT (invoer)</td>
<td>Retourneer de opgegeven invoer, die wordt geconverteerd naar een tekenreeks die wordt opgemaakt volgens de lokale instellingen van de server van het huidige Dynamics 365 for Operations-exemplaar. Voor waarden van het type <strong>real</strong> wordt de tekenreeksconversie beperkt tot twee decimalen.</td>
<td>Als de Dynamics 365 voor bewerkingen exemplaar server landinstelling is gedefinieerd als <strong>EN-US</strong>, <strong>tekst (nu ())</strong> Hiermee wordt de huidige Dynamics 365 voor bewerkingen sessiedatum, 17-12/2015 wordt de tekenreeks <strong>&quot;17-12/2015 07:59:23 AM&quot;</strong>. <strong>TEKST (1/3)</strong> retourneert <strong>&quot;0,33&quot;</strong>.</td>
</tr>
<tr class="even">
<td>FORMAT (tekenreeks 1, tekenreeks 2[, tekenreeks 3, ...])</td>
<td>Retourneer de opgegeven tekenreeks, die wordt opgemaakt door elk exemplaar van <strong>%N</strong> te vervangen door het <em>n</em>de argument. De argumenten zijn tekenreeksen. Als een argument niet is opgegeven voor een parameter, de parameter wordt geretourneerd als <strong>&quot;%n&quot;</strong> in de tekenreeks. Voor waarden van het type <strong>real</strong> wordt de tekenreeksconversie beperkt tot twee decimalen.</td>
<td>In dit voorbeeld retourneert de gegevensbron <strong>PaymentModel</strong> de lijst van klantrecords via het onderdeel <strong>Klant</strong> en de waarde van de verwerkingsdatum via het veld <strong>ProcessingDate</strong>. <a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a>In de Emergency Recovery-indeling dat is ontworpen om een elektronisch bestand genereren voor geselecteerde klanten <strong>PaymentModel</strong> is geselecteerd als een gegevensbron en controleert de processtroom. Er treedt een uitzondering op voor eindgebruikers wanneer een geselecteerde klant wordt gestopt voor de datum waarop het rapport wordt verwerkt. De formule die is ontworpen voor dit type verwerkingsbesturingselement kan de volgende bronnen gebruiken:
<ul>
<li>Dynamics 365 for Operations-label SYS70894, met de volgende tekst:
<ul>
<li><strong>Voor de taal EN-US:</strong>&quot;niets om af te drukken&quot;</li>
<li><strong>Voor de taal van DE:</strong>&quot;Nichts zu drucken&quot;</li>
</ul></li>
<li>Dynamics 365 for Operations-label SYS18389, met de volgende tekst:
<ul>
<li><strong>Voor de taal EN-US:</strong>&quot;klant %1 is geblokkeerd voor %2.&quot;</li>
<li><strong>Voor de taal van DE:</strong>&quot;Debitor '%1' geeft für %2 gesperrt.&quot;</li>
</ul></li>
</ul>
Dit is de formule die kan worden ontworpen: indeling (samenvoegen (@&quot;SYS70894&quot;,&quot;. &quot;@&quot;SYS18389&quot;), model.Customer.Name, DATETIMEFORMAT (model. ProcessingDate, &quot;d&quot;)) als een rapport wordt verwerkt voor de <strong>Litware detailhandelklanten</strong> op 17 december 2015 in de <strong>EN-US</strong> cultuur en de <strong>EN-US</strong> taal, deze formule retourneert de volgende tekst, die als een uitzondering weergegeven voor de eindgebruiker worden weergegeven: &quot;niets om af te drukken. Klant Litware detailhandel wordt voor 17-12/2015 gestopt.&quot; Als het rapport wordt verwerkt voor de<strong> Litware detailhandelklanten</strong> op 17 december 2015 in de <strong>DE</strong> cultuur en de <strong>DE</strong> taal, deze formule resulteert in de volgende tekst die gebruikmaakt van een andere datumnotatie: &quot;Nichts zu drucken. Debitor 'Litware Retail' doorgegeven für 17.12.2015 gesperrt.&quot; <strong>Opmerking: </strong>de volgende syntaxis wordt toegepast in ER-formules voor labels:
<ul>
<li><strong>Voor labels van Dynamics 365 voor bronnen voor bedrijfsactiviteiten:</strong> <strong>@&quot;X&quot;</strong>, waarbij X staat voor de label-ID in de Application Object Tree (AOT)</li>
<li><strong>Voor labels die zich in de configuraties van Emergency Recovery bevinden:</strong> <strong>@&quot;ER_LABEL:X&quot;</strong>, waarbij X staat voor de label-ID in de Emergency Recovery-configuratie</li>
</ul></td>
</tr>
<tr class="odd">
<td>NUMBERFORMAT (getal, indeling)</td>
<td>Retourneer de tekenreeksvoorstelling van het opgegeven getal in de opgegeven indeling. (Zie voor informatie over de ondersteunde indelingen <a href="https://msdn.microsoft.com/en-us/library/dwhawy9k(v=vs.110).aspx">standaard</a> en <a href="https://msdn.microsoft.com/en-us/library/0c899ak8(v=vs.110).aspx">aangepaste</a>.) De context dat deze functie wordt uitgevoerd, bepaalt de cultuur die wordt gebruikt voor het opmaken van nummers.</td>
<td>Voor de cultuur EN-US <strong>NUMBERFORMAT (0,45 &quot;p&quot;)</strong> retourneert <strong>&quot;45,00%&quot;</strong>. <strong>NUMBERFORMAT (10.45, &quot;#&quot;)</strong> retourneert <strong>&quot;10&quot;</strong>.</td>
</tr>
<tr class="even">
<td>NUMERALSTOTEXT (aantal, taal, valuta, naamvlag van valuta afdrukken, aantal decimalen)</td>
<td>Retourneert het uitgeschreven aantal (geconverteerd) in tekenreeksen in de opgegeven taal. De taalcode is optioneel: wanneer deze is gedefinieerd als lege tekenreeks, wordt in plaats daarvan de lopende code van de contexttaal gebruikt (gedefinieerd voor genererende map of bestand). De opgegeven valutacode is optioneel. Wanneer deze als lege tekenreeks is gedefinieerd, wordt de bedrijfsvaluta genomen. Houd er rekening mee dat de parameter <strong>Valutanaam afdrukken</strong> en de parameter<strong>Aantal decimalen</strong> alleen worden geanalyseerd voor de volgende taalcodes: <strong>CS</strong>, <strong>ET</strong>, <strong>HU</strong>, <strong>LT</strong>, <strong>LV</strong>, <strong>PL</strong>, <strong>RU</strong>. Opmerking: de parameter <strong>Valutanaam afdrukken</strong> wordt alleen voor Dynamics 365 for Operations-bedrijven met de context van het land dat de valutaverzwakking ondersteunt.</td>
<td>NUMERALSTOTEXT (1234,56, &quot;EN&quot;, &quot;&quot;, false, 2) retourneert 'One 1000 tweehonderdvierendertig en 56' NUMERALSTOTEXT (120, &quot;PL&quot;, &quot;&quot;, false, 0) retourneert 'Sto dwadzieścia' NUMERALSTOTEXT (120.21, &quot;RU&quot;, &quot;EUR&quot;, waar, 2) retourneert 'евроцент Сто двадцать евро 21'</td>
</tr>
<tr class="odd">
<td>PADLEFT (tekenreeks, lengte, opvultekens)</td>
<td>Retourneert een tekenreeks met een bepaalde lengte waarin het begin van de huidige tekenreeks is aangevuld met opgegeven tekens.</td>
<td>PADLEFT (“1234”, 10, “ “) retourneert de tekstreeks “      1234”</td>
</tr>
</tbody>
</table>

### <a name="data-collection-functions"></a>Functies voor gegevensverzameling

Functie

Omschrijving

Voorbeeld

FORMATELEMENTNAME ()

Geeft de naam van het element van de huidige indeling als resultaat. Retourneert een lege tekenreeks wanneer de markering **Uitvoerdetails verzamelen** van de huidige bestanden wordt uitgeschakeld.

Raadpleeg de taakbegeleider **ER Gegevens van indelingsuitvoer gebruiken voor voor tellen en optellen** (onderdeel van bedrijfsproces **Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen**) voor meer informatie over het gebruik van deze functies.

SOMMEN (tekenreeks voor optellen criteria bereik1, waarde1 criteriumreeks belangrijke \[, criteria bereik2 tekenreeks, waarde2 criteriatekenreeks,... \])

Retourneert een som met waarden van XML-knooppunten (met als sleutel gedefinieerde naam), die tijdens deze indelingsuitvoering is verzameld en voldoet aan de ingevoerde voorwaarden (koppels van bereik en waarde). Retourneert een nulwaarde wanneer de markering **Uitvoerdetails verzamelen **van de de huidige bestanden wordt uitgeschakeld.

SUMIF (sleutelreeks voor optellen, criteriumbereik tekenreeks, criteriumwaarde tekenreeks)

Retourneert een som met waarden van XML-knooppunten (met als sleutel gedefinieerde naam), die tijdens deze indelingsuitvoering is verzameld en voldoet aan de ingevoerde voorwaarde (bereik en waarde). Retourneert een nulwaarde wanneer de markering **Uitvoerdetails verzamelen **van de huidige bestanden wordt uitgeschakeld.

NULWAARDE (Bereik1 criteriumreeks, criteria waarde1 tekenreeks \[, criteria bereik2 tekenreeks, waarde2 criteriatekenreeks,... \])

Retourneert een aantal XML-knooppunten, die tijdens deze indelingsuitvoering is verzameld en voldoet aan de ingevoerde voorwaarden (koppels van bereik en waarde). Retourneert een nulwaarde wanneer de markering **Uitvoerdetails verzamelen **van de huidige bestanden wordt uitgeschakeld.

COUNTIF (criteriumbereik tekenreeks, criteriumwaarde tekenreeks)

Retourneert een aantal XML-knooppunten, dat tijdens deze indelingsuitvoering is verzameld en voldoet aan de ingevoerde voorwaarde (bereik en waarde). Retourneert een nulwaarde wanneer de markering **Uitvoerdetails verzamelen **van de huidige bestanden wordt uitgeschakeld.

COLLECTEDLIST (Bereik1 criteriumreeks, criteria waarde1 tekenreeks \[, criteria bereik2 tekenreeks, waarde2 criteriatekenreeks,... \])

Retourneert een lijst met waarden van XML-knooppunten, die tijdens deze indelingsuitvoering is verzameld en voldoet aan de ingevoerde voorwaarden (bereik en waarde). Retourneert een lege lijst wanneer de markering **Uitvoerdetails verzamelen **van de huidige bestanden wordt uitgeschakeld.

### <a name="other-business-domainspecific-functions"></a>Andere functies (voor specifiek zakelijk domein)

| Functie                                                                         | Omschrijving                                                                                                                                                                                                                                                        | Voorbeeld                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CONVERTCURRENCY (bedrag, bronvaluta, doelvaluta, datum, bedrijf)        | Converteer het opgegeven monetaire bedrag van de bronvaluta naar de doelvaluta door de instellingen van het opgegeven Dynamics 365 for Operations-bedrijf op de opgegeven datum te gebruiken.                                                                            | **CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")** retourneert het equivalent van één euro in Amerikaanse dollars op de huidige sessiedatum, op basis van de instellingen voor het bedrijf DEMF.                                                                                                                                  |
| ROUNDAMOUNT (aantal, decimalen, afrondingsregel)                                       | Rond het opgegeven bedrag af op basis van de opgegeven afrondingsregel en het opgegeven aantal decimalen. **Opmerking:** de afrondingsregel moet worden opgegeven als een waarde van de Dynamics 365 for Operations-opsomming **RoundOffType**.                          | Als de **model. RoundOff** parameter is ingesteld op *** Downward *** **ROUNDAMOUNT (1000.787, 2, model. RoundOff)** retourneert de waarde **1000.78**. Als de parameter **model.RoundOff** is ingesteld op **Normal** of **Rounding-up**, retourneert **ROUNDAMOUNT (1000,787, 2, model.RoundOff)** de waarde **1000,79**. |
| CURCredRef (cijfers)                                                              | Retourneer een crediteurverwijzing op basis van de cijfers van het opgegeven factuurnummer.                                                                                                                                                                                  | **CURCredRef ("VEND-200002")** retourneert **"2200002"**.                                                                                                                                                                                                                                                         |
| REST\_97 (cijfers)                                                                 | Retourneer een crediteurverwijzing als een MOD97-expressie op basis van de cijfers van het opgegeven factuurnummer.                                                                                                                                                            | **REST\_97 ('leverancier-200002')** retourneert **'20000285'**.                                                                                                                                                                                                                                                           |
| ISOCredRef (cijfers)                                                              | Retourneer een ISO-crediteurverwijzing op basis van de cijfers en alfabetische symbolen van het opgegeven factuurnummer. **Opmerking: **als u symbolen wilt elimineren uit alfabetten die niet ISO-conform zijn, moet de invoerparameter worden vertaald voordat deze wordt doorgegeven aan deze functie. | **ISOCredRef ("VEND-200002")** retourneert **"RF23VEND-200002"**.                                                                                                                                                                                                                                                 |
| CN\_GBT\_AdditionalDimensionID (tekenreeks, getal)                                  | Haal de aanvullende financiële dimensie-id op. Dimensies worden in deze reeks vertegenwoordigd als id's die door komma's gescheiden zijn. De getallen definiëren de gewenste volgordecode van de dimensie in deze reeks.                                                                            | CN\_GBT\_AdditionalDimensionID ('AA, BB, CC, DD, EE, FF, GG, uu', 3) 'CC' retourneren                                                                                                                                                                                                                                      |
| GetCurrentCompany ()                                                             | Retourneert de code van het huidige geregistreerde bedrijf.                                                                                                                                                                                                                    |                                                                                                                                                                                                                                                                                                               |
| CH\_BANK\_MOD\_10 (cijfers)                                                       | Retourneert een crediteurverwijzing als een MOD10-expressie op basis van de cijfers van het opgegeven factuurnummer.                                                                                                                                                                      | CH\_BANK\_MOD\_10 ('leverancier-200002') retourneert 3                                                                                                                                                                                                                                                                   |
| FA\_som (vaste activa-code, waardecode model, begindatum, einddatum)               | Retourneert de voorbereide gegevenscontainer van vaste-activabedragen voor een periode.                                                                                                                                                                                         | FA\_som ('COMP 000001', 'Huidige', datum1, datum2) geeft als resultaat de container voorbereide gegevens van het vaste activum 'COMP 000001' met het waardemodel 'Huidige' voor een periode van Datum1 datum2.                                                                                                                        |
| FA\_(voor vaste activa-code, model waardecode rapportjaar, Aangiftedatum) | Retourneert de voorbereide gegevenscontainer van vaste-activasaldi. Het rapportjaar moet zijn gespecificeerd als waarde van een Dynamics 365 for Operations-opsomming **AssetYear**.                                                                                           | FA\_som ('COMP 000001', 'Huidige', AxEnumAssetYear.ThisYear, SESSIONTODAY ()) resulteert de voorbereide gegevenscontainer van saldi voor het vaste activum 'COMP-000001' met het waardemodel 'Huidige' op de huidige 365 voor bewerkingen sessiedatum.                                                                |

### <a name="functions-list-extension"></a>Uitbreiding lijst met functies

MET ER kunt u de lijst met functies uitbreiden die in ER-expressies worden gebruikt. Hiervoor is enige mate van engineering vereist. Zie voor gedetailleerde informatie [De lijst met functies voor elektronische rapportage uitbreiden](general-electronic-reporting-formulas-list-extension.md).

<a name="see-also"></a>Zie ook
--------

[Overzicht van elektronische rapportage](general-electronic-reporting.md)

[De lijst met functies voor elektronische rapportage (ER) uitbreiden](general-electronic-reporting-formulas-list-extension.md)


