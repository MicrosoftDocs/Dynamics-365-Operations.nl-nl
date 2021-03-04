---
title: Formuletaal in Elektronische rapportage
description: Dit onderwerp biedt algemene informatie over het gebruik van de formuletaal in ER (Elektronische rapportage).
author: NickSelin
manager: kfend
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b3f11e91d06f20d1c384c3c2c5cf9326214331ee
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686264"
---
# <a name="electronic-reporting-formula-language"></a>Formuletaal in Elektronische rapportage

[!include [banner](../includes/banner.md)]

ER biedt een krachtige ervaring voor gegevenstransformatie. De taal die wordt gebruikt om de vereiste gegevensbewerkingen in de [ER-formuleontwerper](general-electronic-reporting-formula-designer.md) uit te drukken, lijkt op de formuletaal in Microsoft Excel.

## <a name="basic-syntax"></a>Basissyntaxis

ER-expressies kunnen een of alle van de volgende elementen bevatten:

- [Constanten](#Constants)
- [Operatoren](#Operators)
- [Verwijzingen](#References)
- [Paden](#Paths)
- [Functies](#Functions)

## <a name=""></a><a name="Constants">Constanten</a>

Wanneer u expressies ontwerpt, kunt u tekst- en numerieke constanten (waarden die niet worden berekend) gebruiken. De expressie `VALUE ("100") + 20` gebruikt bijvoorbeeld de numerieke constante **20** en de tekenreeksconstante **'100'** en retourneert de numerieke waarde **120**.

De ER-formuleontwerper ondersteunt escapereeksen. Daarom kunt u een expressiereeks opgeven die anders moet worden behandeld. De expressie `"Leo Tolstoy ""War and Peace"" Volume 1"` retourneert bijvoorbeeld de tekstreeks **Leo Tolstoy "War and Peace" Volume 1**.

## <a name=""></a><a name="Operators">Operatoren</a>

De volgende tabel toont de rekenkundige operators die u kunt gebruiken om wiskundige basisbewerkingen uit te voeren, zoals optelling, aftrekking, deling en vermenigvuldiging.

| Operator | Betekenis               | Voorbeeld     |
|----------|-----------------------|-------------|
| +        | Optelling              | `1+2`       |
| -        | Aftrekking, negatie | `5-2`, `-1` |
| \*       | Vermenigvuldigen        | `7\*8`      |
| /        | Afdeling              | `9/3`       |

De volgende tabel geeft de vergelijkingsoperatoren weer die worden ondersteund. U kunt deze operatoren gebruiken om twee waarden te vergelijken.

| Operator | Betekenis                  | Voorbeeld      |
|----------|--------------------------|--------------|
| =        | Gelijk                    | `X=Y`        |
| &gt;     | Groter dan             | `X>Y`        |
| &lt;     | Kleiner dan                | `X<Y`        |
| &gt;=    | Groter dan of gelijk aan | `X>=Y`       |
| &lt;=    | Kleiner dan of gelijk aan    | `X<=Y`       |
| &lt;&gt; | Niet gelijk aan             | `X<>Y`       |

Bovendien kunt u een ampersandteken (&) als tekstsamenvoegingsoperator gebruiken. Op deze manier kunt u twee tekstreeksen verbinden of samenvoegen tot één tekst.

| Operator | Betekenis     | Voorbeeld                                               |
|----------|-------------|-------------------------------------------------------|
| &        | Samenvoegen | `"Nothing to print:" & " " & "no records found"`      |

### <a name="operator-precedence"></a>Operatorprioriteit

De volgorde waarin de onderdelen van een samenstellingsexpressie worden geëvalueerd, is belangrijk. Het resultaat van de expressie `1 + 4 / 2` verschilt bijvoorbeeld, afhankelijk van of de optellings- of deelbewerking eerst wordt uitgevoerd. U kunt haakjes gebruiken om expliciet te definiëren hoe een expressie wordt geëvalueerd. Als u bijvoorbeeld wilt aangeven dat de optellingsbewerking eerst moet worden uitgevoerd, kunt u de voorafgaande expressie wijzigen in `(1 + 4) / 2`. Als u de volgorde van bewerkingen die moeten worden uitgevoerd in een expressie, niet expliciet aangeeft, wordt de volgorde gebaseerd op de standaardprioriteit die aan de ondersteunde operators is toegewezen. De volgende tabel toont de operators en de prioriteit die eraan is toegewezen. Operators met een hogere prioriteit (bijvoorbeeld 7) worden eerder geëvalueerd dan operators met een lagere prioriteit (bijvoorbeeld 1).

| Prioriteit | Operatoren      | Syntaxis                                                                  |
|------------|----------------|-------------------------------------------------------------------------|
| 7          | Groepering       | ( … )                                                                   |
| 6          | Toegankelijkheid voor leden  | … . …                                                                   |
| 5          | Functieaanroep  | … ( … )                                                                 |
| 4          | Vermenigvuldigen | … \* …<br>… / …                                                         |
| 3          | Additief       | … + …<br>… - …                                                          |
| 2          | Vergelijking     | … &lt; …<br>… &lt;= …<br>… =&gt; …<br>… &gt; …<br>… = …<br>… &lt;&gt; … |
| 1          | Scheidingsteken     | … , …                                                                   |

Als een expressie meerdere opeenvolgende operatoren met dezelfde prioriteit bevat, worden die bewerkingen van links naar rechts geëvalueerd. De expressie `1 + 6 / 2 \* 3 > 5` retourneert bijvoorbeeld **waar**. We raden aan haakjes te gebruiken om de gewenste evaluatievolgorde van bewerkingen in expressies expliciet aan te geven, zodat de expressies gemakkelijker te lezen en onderhouden zijn.

## <a name=""></a><a name="References">Verwijzingen</a>

Alle gegevensbronnen van het huidige ER-onderdeel die tijdens het ontwerp van een expressie beschikbaar zijn, kunnen als benoemde verwijzingen worden gebruikt. Het huidige ER-onderdeel kan een modeltoewijzing of een indeling zijn. De huidige ER-modeltoewijzing bevat bijvoorbeeld de gegevensbron **ReportingDate** die een waarde van het gegevenstype *DateTime* retourneert. Om te zorgen dat deze waarde juist wordt opgemaakt in het genererende document kunt u als volgt verwijzen naar de gegevensbron in de expressie: `DATETIMEFORMAT (ReportingDate, "dd-MM-yyyy")`.

Alle tekens in de naam van een verwijzende gegevensbron die niet staan voor een letter van het alfabet, moeten worden voorafgegaan door een enkel aanhalingsteken ('). Als de naam van een verwijzende gegevensbron ten minste één symbool bevat dat geen letter van het alfabet voorstelt, moet de naam tussen enkele aanhalingstekens staan. Deze niet-alfabetische symbolen kunnen bijvoorbeeld leestekens of andere geschreven symbolen zijn. Hieronder vindt u enkele voorbeelden:

- In een ER-expressie moet als volgt naar de gegevensbron **Datum en tijd van vandaag** worden verwezen: `'Today''s date & time'`
- Naar de methode **name()** van de gegevensbron **Klanten** moet in een ER-expressie als volgt worden verwezen: `Customers.'name()'`.

Als de methoden van toepassingsgegevensbronnen parameters hebben, wordt de volgende syntaxis gebruikt om deze methoden aan te roepen:

- Naar de methode **isLanguageRTL** van de gegevensbron **Systeem** met een parameter **EN-US** van het gegevenstype *Tekenreeks* moet in een ER-expressie als volgt worden verwezen: `System.isLanguageRTL("EN-US")`.
- Aanhalingstekens zijn niet verplicht wanneer een methodenaam alleen alfanumerieke tekens bevat. Ze zijn wel verplicht voor een methode van een tabel als de naam haakjes bevat.

Als de gegevensbron **Systeem** wordt toegevoegd aan een ER-toewijzing die naar de toepassingsklasse **Global** verwijst, retourneert de expressie `System.isLanguageRTL("EN-US ")` de *Booleaanse* waarde **FALSE**. De gewijzigde expressie `System.isLanguageRTL("AR")` retourneert de *Booleaanse* waarde **TRUE**.

U kunt de manier waarop waarden worden doorgegeven aan de parameters van dit type methode beperken:

- Alleen constanten kunnen worden doorgegeven aan methoden van dit type. De waarden van de constanten worden gedefinieerd in de ontwerpfase.
- Alleen primitieve (basis) gegevenstypen worden voor parameters van dit type ondersteund. De primitieve gegevenstypen zijn *Geheel getal*, *Werkelijk*, *Booleaans* en *Tekenreeks*.

## <a name=""></a><a name="Paths">Paden</a>

Wanneer een expressie naar een gestructureerde gegevensbron verwijst, kunt u de paddefinitie gebruiken om een specifiek primitief element van deze gegevensbron te selecteren. Een puntteken (.) wordt gebruikt om afzonderlijke individuele elementen van een gestructureerde gegevensbron te scheiden. De huidige ER-modeltoewijzing bevat bijvoorbeeld de gegevensbron **InvoiceTransactions** die een lijst met records retourneert. De recordstructuur **InvoiceTransactions** bevat de velden **AmountDebit** en **AmountCredit**, die beide numerieke waarden retourneren. U kunt daarom de volgende expressie ontwerpen om het gefactureerde bedrag te berekenen: `InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit`. De constructie `InvoiceTransactions.AmountDebit` in deze expressie is het pad dat wordt gebruikt voor toegang tot het veld **AmountDebit** van de gegevensbron **InvoiceTransactions** van het type *Recordlijst*.

### <a name="relative-path"></a>Relatief pad

Als het pad van een gestructureerde gegevensbron begint met een apenstaartje (@), is dit een relatief pad. Het apenstaartje wordt weergegeven in plaats van het resterende deel van het absolute pad van de hiërarchische boomstructuur die wordt gebruikt. In de volgende afbeelding ziet u een voorbeeld. Hier geeft het absolute pad `Ledger.'accountingCurrency()'` aan dat de waarde van de valuta voor boekhouding uit de gegevensbron **Grootboek** wordt ingevoerd in het veld **AccountingCurrency** van het gegevensmodel.

![Voorbeeld van een absoluut pad op de pagina ER-modeltoewijzing ontwerpen](./media/ER-FormulaLanguage-AbsolutePath.png)

In het voorbeeld in de volgende afbeelding ziet u hoe een relatief pad wordt gebruikt. Het relatieve pad `@.AccountNum` geeft aan dat het veld **AccountNum** van de gegevensbron **Intrastat** (die één niveau boven het veld **AccountNum** in de hiërarchische structuur van het gegevensmodel wordt weergegeven) wordt gebruikt om het klant- of leverancierrekeningnummer in te voeren in het veld **AccountNum** van het gegevensmodel.

![Voorbeeld van een relatief pad op de pagina ER-modeltoewijzing ontwerpen](./media/ER-FormulaLanguage-RelativePath1.png)

Het resterende gedeelte van het absolute pad wordt ook weergegeven in de [ER-formule-editor](general-electronic-reporting-formula-designer.md).

![Resterend gedeelte van het absolute pad op de pagina ER-formuleontwerper](./media/ER-FormulaLanguage-RelativePath2.png)

Zie [Een relatief pad gebruiken in gegevensbindingen van ER-modellen en -indelingen](relative-path-data-bindings-er-models-format.md) voor meer informatie.

## <a name=""></a><a name="Functions">Functies</a>

Ingebouwde ER-functies kunnen worden gebruikt in ER-expressies. Alle gegevensbronnen van de expressiecontext (de huidige ER-modeltoewijzing of de huidige ER-indeling) en ook constanten kunnen als parameters worden gebruikt van functieaanroepen volgens de lijst met argumenten voor functieaanroepen. Constanten kunnen ook worden gebruikt als parameters van het aanroepen van functies. De huidige ER-modeltoewijzing bevat bijvoorbeeld de gegevensbron **InvoiceTransactions** die een lijst met records retourneert. De recordstructuur **InvoiceTransactions** bevat de velden **AmountDebit** en **AmountCredit**, die beide numerieke waarden retourneren. Voor het berekenen van het gefactureerde bedrag kunt u daarom de volgende expressie ontwerpen die de ingebouwde ER-afrondingsfunctie gebruikt: `ROUND (InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit, 2)`.

Wanneer u ER-modeltoewijzingen en ER-rapporten ontwerpt, kunt u ER-functies uit de volgende categorieën gebruiken:

- [Datum- en tijdfuncties](er-functions-category-datetime.md)
- [Lijstfuncties](er-functions-category-list.md)
- [Logische functies](er-functions-category-logical.md)
- [Wiskundige functies](er-functions-category-mathematical.md)
- [Registratiefuncties](er-functions-category-record.md)
- [Tekstfuncties](er-functions-category-text.md)
- [Functies voor gegevensverzameling](er-functions-category-data-collection.md)
- [Andere functies (voor specifiek zakelijk domein)](er-functions-category-other.md)
- [Type conversiefuncties](er-functions-category-type-conversion.md)

## <a name="functions-list-extension"></a>Uitbreiding lijst met functies

MET ER kunt u de lijst met functies uitbreiden die in ER-expressies worden gebruikt. Hiervoor is enige mate van engineering vereist. Zie voor gedetailleerde informatie [De lijst met functies voor elektronische rapportage (ER) uitbreiden](general-electronic-reporting-formulas-list-extension.md).

## <a name="compound-expressions"></a>Samengestelde expressies

U kunt samengestelde expressies maken die gebruikmaken van functies uit verschillende categorieën, op voorwaarde dat de gegevenstypen overeenkomen. Wanneer u functies samen gebruikt, moet het gegevenstype van de uitvoer van de ene functie overeenkomen met het invoergegevenstype dat vereist is voor een andere functie. Als u bijvoorbeeld een mogelijke fout over een lege wilt voorkomen in een binding van een veld aan een ER-indelingselement, combineert u functies uit de categorie [List](er-functions-category-list.md) met een functie uit de categorie [Logical](er-functions-category-logical.md), zoals in het volgende voorbeeld wordt getoond. Hier gebruikt de formule de functie [IF](er-functions-logical-if.md) om te testen of de lijst **IntrastatTotals** leeg is voordat deze de waarde van de vereiste aggregatie uit die lijst retourneert. Als de lijst **IntrastatTotals** leeg is, retourneert de formule **0** (nul).

```vb
IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded') 
```

## <a name="multiple-solutions"></a>Meerdere oplossingen

Vaak kunt u hetzelfde resultaat voor gegevenstransformatie op meerdere manieren krijgen door functies uit verschillende categorieën of verschillende functies uit dezelfde categorie te gebruiken. De vorige expressie kan bijvoorbeeld ook worden geconfigureerd met de functie [COUNT](er-functions-list-count.md) uit de categorie [List](er-functions-category-list.md).

```vb
IF(COUNT (IntrastatTotals)=0, 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded') 
```

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht van elektronische rapportage](general-electronic-reporting.md)

[Formuleontwerper in elektronische aangifte](general-electronic-reporting-formula-designer.md)

[De lijst met functies voor elektronische rapportage uitbreiden](general-electronic-reporting-formulas-list-extension.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]