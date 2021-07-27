---
title: Ondersteunde primitieve gegevenstypen voor formules voor elektronische rapportage
description: Dit onderwerp biedt informatie over de primitieve gegevenstypen die worden ondersteund in ER-formules (Elektronische rapportage).
author: NickSelin
ms.date: 06/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4e1c70dd0fa89c6cc5a8b4778b073d1cf4a3dadd
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/06/2021
ms.locfileid: "6355317"
---
# <a name="supported-primitive-data-types-for-electronic-reporting-formulas"></a>Ondersteunde primitieve gegevenstypen voor formules voor elektronische rapportage

[!include [banner](../includes/banner.md)]

Dit onderwerp biedt informatie over de primitieve gegevenstypen die worden ondersteund in expressies voor [Elektronische rapportage (ER)](general-electronic-reporting.md). Hier volgt een lijst van de primitieve gegevenstypen:

- [booleaans](#boolean)
- [datum](#date)
- [datum/tijd](#datetime)
- [opsomming](#enumeration)
- [guid](#guid)
- [geheel getal](#integer)
- [int64](#int64)
- [real](#real)
- [tekenreeks](#string)

## <a name="boolean"></a><a name="boolean"></a>Booleaans

Het *booleaanse* primitieve gegevenstype bevat een waarde die als *waar* of *onwaar* wordt geëvalueerd. U kunt de gereserveerde letterlijke trefwoorden **Waar** en **Onwaar** gebruiken waar een *booleaanse* expressie wordt verwacht. De standaardwaarde is *onwaar*.

De interne weergave van een *booleaanse* waarde is een *geheel getal*. De waarde van het *gehele getal* 0 (nul) wordt als *onwaar* geëvalueerd en alle andere waarden van *geheel getal* worden als *waar* geëvalueerd. Wanneer u een geconfigureerde expressie [valideert](general-electronic-reporting-formula-designer.md#TestFormula) die een *booleaanse* waarde retourneert in de [ER-formuleontwerper](er-advanced-formula-editor.md), wordt in het testresultaatvenster *0* (nul) weergegeven wanneer een expressie *onwaar* resulteert. Anders wordt in het testresultaatvenster *1* weergegeven.

Een *booleaanse* waarde heeft geen impliciete conversies. U kunt de functie [TEXT](er-functions-text-text.md) gebruiken om een *booleaanse* waarde expliciet te converteren naar een *tekenreeks*:

- De waarde *onwaar* wordt geconverteerd naar de tekstreeks **Onwaar**.
- De waarde *waar* wordt geconverteerd naar de tekstreeks **Waar**.

> [!NOTE]
> Deze conversie is niet afhankelijk van de opgegeven taal- en cultuur[context](er-design-multilingual-reports.md).

Vergelijkings [operators](er-formula-language.md#Operators) zijn het enige operatortype dat kan worden gebruikt met het *booleaanse* gegevenstype. De volgende operators kunnen worden gebruikt om twee *booleaanse* waarden te vergelijken: \<\> en =.

## <a name="date"></a><a name="date"></a>Datum

Het primitieve gegevenstype *datum* bevat de dag, de maand en het jaar. Datums kunnen worden geïnitieerd met de volgende functies:

- [DATEVALUE](er-functions-datetime-datevalue.md)
- [NULLDATE](er-functions-datetime-nulldate.md)
- [SESSIONTODAY](er-functions-datetime-sessiontoday.md)
- [TODAY](er-functions-datetime-today.md)

Het gegevenstype *datum* kan datums bevatten tussen 1 januari 1900 en 31 december 2154. De standaardwaarde is **nul** en de interne weergave is de datum 1 januari 1900.

Een *datum* heeft geen impliciete conversies. U kunt echter de volgende expliciete conversiefuncties gebruiken:

- [DATEFORMAT](er-functions-datetime-dateformat.md)
- [DATETODATETIME](er-functions-datetime-datetodatetime.md)
- [TEXT](er-functions-text-text.md)

Met de functie [ADDDAYS](er-functions-datetime-adddays.md) kunt u dagen optellen bij en aftrekken van datums. Op deze manier kunt u de datum met een bepaald aantal dagen in de toekomst en het verleden verplaatsen. Met de functie [DAYS](er-functions-datetime-days.md) kunt u datums van elkaar aftrekken en het verschil in dagen berekenen. Zie [Lijst met ER-functies in de categorie Datum en tijd](er-functions-category-datetime.md) voor meer informatie over de transformatie van waarden voor *datum*.

Vergelijkings [operators](er-formula-language.md#Operators) zijn het enige operatortype dat kan worden gebruikt met het gegevenstype *datum*. De volgende operators kunnen worden gebruikt om twee waarden voor *datum* te vergelijken: \<\>, \<, \<=, =, \> en \>=.

## <a name="datetime"></a><a name="datetime"></a>Datum/tijd

Met het primitieve gegevenstype *datum/tijd* worden het type *datum* en een waarde gecombineerd die staan voor de tijd die sinds middernacht is verstreken. De tijd wordt uitgedrukt in uren, minuten, seconden en fracties van een seconde. Een waarde voor *datum/tijd* bevat ook informatie over de tijdzone.

Het gegevenstype *datum/tijd* kan datums bevatten tussen 1 januari 1900 (1900-01-01T00:00:00.0000000+00:00 in de round trip-[notatie)](/dotnet/standard/base-types/standard-date-and-time-format-strings) en 31 december 2154 (2154/12/31T11:59:59.9999999+00:00 in de round trip-notatie). De kleinste tijdseenheid voor *datum/tijd* is één tien miljoenste van een seconde.

> [!NOTE]
> Wanneer de **uu**-[specificatie](/dotnet/standard/base-types/standard-date-and-time-format-strings) wordt gebruikt voor uren, kunnen tijdwaarden boven 12:59:59:9999999 niet als geldige tijden worden geïnterpreteerd.
>
> Wanneer de **UU**-specificatie wordt gebruikt voor uren, kunnen tijdwaarden boven 23:59:59:9999999 niet als geldige tijden worden geïnterpreteerd.

De standaardwaarde is **null** en de interne weergave is de datum 1 januari 1900 (1900-01-01T00:00:00.0000000+00:00 in de round trip-notatie).

Waarden voor datum/tijd kunnen worden geïnitieerd met de volgende functies:

- [DATETIMEVALUE](er-functions-datetime-datetimevalue.md)
- [NULNULLDATETIMELDATE](er-functions-datetime-nulldatetime.md)
- [SESSIONNOW](er-functions-datetime-sessionnow.md)
- [NOW](er-functions-datetime-now.md)

Een *datum/tijd* heeft geen impliciete conversies. U kunt echter de volgende expliciete conversiefuncties gebruiken:

- [DATETIMEFORMAT](er-functions-datetime-datetimeformat.md)
- [TEXT](er-functions-text-text.md)

Zie [Lijst met ER-functies in de categorie Datum en tijd](er-functions-category-datetime.md) voor meer informatie over de transformatie van waarden voor *datum/tijd*.

Vergelijkings [operators](er-formula-language.md#Operators) zijn het enige operatortype dat kan worden gebruikt met het gegevenstype *datum/tijd*. De volgende operators kunnen worden gebruikt om twee waarden voor *datum/tijd* te vergelijken: \<\>, \<, \<=, =, \> en \>=.

## <a name="enumeration"></a><a name="enumeration"></a>Opsomming

Het primitieve gegevenstype *opsomming* is een lijst met letterlijke waarden. U kunt opsommingen gebruiken die in de [broncode](../dev-ref/xpp-data-primitive.md#enum) van de toepassing zijn gedefinieerd. U kunt ook uw eigen opsommingen introduceren in de onderdelen [ER-gegevensmodel](general-electronic-reporting.md#data-model-and-model-mapping-components) en [ER-indeling](general-electronic-reporting.md#FormatComponentOutbound).

Een *opsomming* van toepassingen kan worden gebruikt in expressies van elke ER-modeltoewijzing en ER-indeling.

In de volgende afbeelding ziet u hoe u de opsomming voor het model **CustVendCorrectiveReasonCode** kunt toevoegen aan het bewerkbare ER-gegevensmodel.

[![Een modelopsomming configureren in de ontwerper van het ER-gegevensmodel.](./media/er-formula-supported-data-types-primitive-enum1.gif)](./media/er-formula-supported-data-types-primitive-enum1.gif)

Een *opsomming* voor model kan worden gebruikt in expressies van elke ER-modeltoewijzing en ER-indeling die zijn gemaakt op basis van een gegevensmodel waarbij de *opsomming* is geïntroduceerd.

In de volgende afbeelding ziet u hoe u de opsomming van de indeling **Lijst met Natura-subcategorieën voor omgekeerde toeslag** kunt toevoegen aan de bewerkbare ER-indeling.

[![Een opsomming voor indeling configureren in de ontwerper van de ER-indeling.](./media/er-formula-supported-data-types-primitive-enum2.gif)](./media/er-formula-supported-data-types-primitive-enum2.gif)

Een *opsomming* voor indeling kan alleen worden gebruikt in expressies van de ER-indeling waar de *opsomming* is geïntroduceerd.

U moet het juiste type ER-gegevensbronnen gebruiken om een specifieke opsomming naar een geconfigureerd ER-onderdeel als een constante of als een waarde te brengen die de gebruiker die een ER-oplossing uitvoert, tijdens runtime in het dialoogvenster heeft gedefinieerd.

- Tot opsommingen voor toepassingen kan toegang worden verkregen met behulp van de gegevensbronnen **Dynamics 365 for Operations \ Opsomming** en **Algemeen \ Gebruikersinvoerparameters**. In de volgende afbeelding ziet u hoe u aan de bewerkbare ER-indeling de gegevensbronnen **appenumNoYes** en **uipNoYes** kunt toevoegen die verwijzen naar de toepassingsopsomming **NoYes**.

    [![Gegevensbronnen voor opsomming van toepassingen toevoegen in de ontwerper van de ER-indeling.](./media/er-formula-supported-data-types-primitive-enum3a.gif)](./media/er-formula-supported-data-types-primitive-enum3a.gif)

- Tot opsommingen voor gegevensmodellen kan toegang worden verkregen met behulp van de gegevensbronnen **Gegevensmodel \ Opsomming** en **Gegevensmodel \ Gebruikersinvoerparameters opsomming**. In de volgende afbeelding ziet u hoe u aan de bewerkbare ER-indeling de gegevensbron **CustVendCorrectiveReasonCode** kunt toevoegen die verwijst naar de gegevensmodelopsomming **CustVendCorrectiveReasonCode**.

    [![Gegevensbronnen voor opsomming van modellen toevoegen in de ontwerper van de ER-indeling.](./media/er-formula-supported-data-types-primitive-enum3b.gif)](./media/er-formula-supported-data-types-primitive-enum3b.gif)

- Tot opsommingen voor indelingen kan toegang worden verkregen met behulp van de gegevensbronnen **Indeling \ Opsomming** en **Indeling \ Gebruikersinvoerparameters opsomming**. In de volgende afbeelding ziet u hoe u aan de bewerkbare ER-indeling de gegevensbron **NaturaReverseCharge** kunt toevoegen die verwijst naar de indelingsopsomming **Natura-subcategorieën omgekeerde toeslag**.

    [![Gegevensbronnen voor opsomming van indelingen toevoegen in de ontwerper van de ER-indeling.](./media/er-formula-supported-data-types-primitive-enum3c.gif)](./media/er-formula-supported-data-types-primitive-enum3c.gif)

Een *opsomming* heeft geen impliciete conversies. U kunt echter de functie [TEXT](er-functions-text-text.md) voor conversie gebruiken om een *opsomming* te converteren naar een tekstreeks. Deze conversie is niet taalafhankelijk. Zie de gebruiksvoorbeelden voor de functies [LISTOFFIELDS](er-functions-list-listoffields.md) en [GETENUMVALUEBYNAME](er-functions-text-getenumvaluebyname.md) voor meer informatie over hoe u een waarde voor *opsomming* kunt koppelen aan de juiste taalspecifieke labels.

Vergelijkings [operators](er-formula-language.md#Operators) zijn het enige operatortype dat kan worden gebruikt met het gegevenstype *opsomming*. De volgende operators kunnen worden gebruikt om twee waarden voor *opsomming* te vergelijken: \<\> en =.

## <a name="guid"></a><a name="guid"></a>Guid

Het primitieve gegevenstype *guid* bevat een GUID-waarde (Globally Unique Identifier). Een GUID is een waarde die op alle computers en netwerken kan worden gebruikt waar een unieke identificatie vereist is. Het is onwaarschijnlijk dat het nummer wordt gedupliceerd. Een geldige GUID voldoet aan alle volgende specificaties:

- Er moeten 32 hexadecimale cijfers zijn.
- Daarnaast moeten er vier liggende streepjes zijn ingesloten op de volgende locaties: 8-4-4-4-12.
- Daarnaast kunnen optionele accolades \{\} aan het begin en einde van de tekenreeks worden toegevoegd. Zo zijn **\{2CDB0FE7-D7B3-4938-A0F0-FE28FB8FE212\}** en **2CDB0FE7-D7B3-4938-A0F0-FE28FB8FE212** beide geldige GUID-tekenreeksen.
- Er moeten dus in totaal 36 of 38 tekens zijn, afhankelijk van de vraag of er accolades worden toegevoegd.
- De letters die als hexadecimale cijfers worden gebruikt, kunnen hoofdletters (A–F), kleine letters (a-f) of een mix hiervan zijn.

De volgende expliciete conversiefuncties kunnen worden gebruikt:

- [GUIDVALUE](er-functions-text-guidvalue.md)
- [TEXT](er-functions-text-text.md)

Vergelijkings [operators](er-formula-language.md#Operators) zijn het enige operatortype dat kan worden gebruikt met het gegevenstype *guid*. De volgende operators kunnen worden gebruikt om twee waarden voor *guid* te vergelijken: \<\> en =.

## <a name="integer"></a><a name="integer"></a>Geheel getal

Het primitieve gegevenstype *geheel getal* staat voor een getal zonder decimalen. Gehele getallen worden als controlevariabelen in herhalende overzichten of als indexen in recordlijsten gebruikt.

Een letterlijke waarde voor *geheel getal* is het gehele getal dat rechtstreeks in een ER-[expressie](general-electronic-reporting-formula-designer.md#formula-designer-overview) (formule) wordt ingevoerd, bijvoorbeeld **12345**. Een *geheel getal* is 32 bits breed. De standaardwaarde is **0** en de interne weergave is een lang getal. Een *geheel getal* wordt automatisch geconverteerd naar een *real*.

Daarnaast kunnen de volgende expliciete conversiefuncties worden gebruikt:

- [INTVALUE](er-functions-conversion-intvalue.md)
- [NUMBERFORMAT](er-functions-text-numberformat.md)
- [TEXT](er-functions-text-text.md)

Het bereik van een *geheel getal* is \[-2,147,483,647 : 2,147,483,647\]. Alle gehele getallen van dit bereik kunnen als letterlijke waarden worden gebruikt.

Alle vergelijkings- en wiskundige [operators](er-formula-language.md#Operators) kunnen worden gebruikt met het gegevenstype *geheel getal*.

## <a name="int64"></a><a name="int64"></a>Int64

Het primitieve gegevenstype *int64* staat voor een getal zonder decimalen. *Int64*-waarden worden als controlevariabelen in herhalende overzichten of als record-id´s gebruikt.

Een *int64* is 64 bits breed. De standaardwaarde is **0** en de interne weergave is een lang getal. Een *int64* wordt automatisch geconverteerd naar een *real*.

Daarnaast kunnen de volgende expliciete conversiefuncties worden gebruikt:

- [INT64VALUE](er-functions-conversion-int64value.md)
- [NUMBERFORMAT](er-functions-text-numberformat.md)
- [TEXT](er-functions-text-text.md)

Het bereik van een *int64* is \[-9,223,372,036,854,775,807 : 9,223,372,036,854,775,807\].

Alle vergelijkings- en wiskundige [operators](er-formula-language.md#Operators) kunnen worden gebruikt met het gegevenstype *int64*.

## <a name="real"></a><a name="real"></a>Real-modus

Het primitieve gegevenstype *real* kan decimale waarden bevatten naast gehele getallen. U kunt decimale letterlijke waarden overal gebruiken waar een *real*-waarde wordt verwacht. Een decimale letterlijke waarde is de decimale waarde zoals die direct in code wordt ingevoerd, bijvoorbeeld **2,19**.

> [!NOTE]
> In ER-expressies wordt een komma (,) altijd als decimaalteken gebruikt.

Reals kunnen in alle expressies worden gebruikt en kunnen met vergelijkings- en rekenkundige operators worden gebruikt. Een *real* heeft een precisie van 16 significante cijfers. De standaardwaarde voor een *real* is **0,0** en de interne weergave is een BCD-getal (Binair-coded Digital). De BCD-codering maakt exacte weergaven mogelijk van waarden die veelvouden zijn van 0,1. Het bereik van een *real*-variabele is -(10)<sup>127</sup> tot en met (10)<sup>127</sup>. Alle real-waarden in dit bereik kunnen worden gebruikt als letterlijke waarden in ER-expressies.

Een *real* heeft geen impliciete conversies. U kunt echter met de volgende functies een *real* expliciet naar andere gegevenstypen converteren en andere gegevenstypen naar een *real*:

- [INTVALUE](er-functions-conversion-intvalue.md)
- [INT64VALUE](er-functions-conversion-int64value.md)
- [NUMBERFORMAT](er-functions-text-numberformat.md)
- [TEXT](er-functions-text-text.md)
- [VALUE](er-functions-conversion-value.md)

Alle vergelijkings- en wiskundige [operators](er-formula-language.md#Operators) kunnen worden gebruikt met het gegevenstype *real*.

## <a name="string"></a><a name="string"></a>Tekenreeks

Het primitieve gegevenstype *tekenreeks* vertegenwoordigt een reeks tekens die worden gebruikt als teksten, rekeningnummers, adressen en telefoonnummers.

Letterlijke waarden voor *tekenreeks* zijn tekens die tussen aanhalingstekens staan (""). Letterlijke waarden voor *tekenreeks* kunnen worden gebruikt waar waarden voor *tekenreeks* worden verwacht in ER-expressies. U kunt tekenreeksen gebruiken in logische expressies, zoals vergelijkingen. U kunt waarden voor *tekenreeks* ook samenvoegen met de operator **\&** of de functie [CONCATENATE](er-functions-text-concatenate.md).

> [!NOTE]
> Als u twee waarden voor *tekenreeks* samenvoegt en u wilt dat de resulterende *tekenreeks* meerdere regels omvat, gebruikt u het scheidingsteken voor regelafbreking tussen de waarden. Voor de TEXT-uitvoer kan dit scheidingsteken een teken zijn dat wordt gegenereerd met de expressie [CHAR](er-functions-text-char.md)(10) of CHAR(13). Voor HTML kan dit het label **\<br\>** zijn.

De standaardwaarde voor een *tekenreeks* is een lege tekenreeks die geen tekens bevat en de interne weergave is een lijst met tekens.

Er zijn geen automatische conversies voor tekenreeksen. De volgende expliciete conversiefuncties kunnen echter worden gebruikt:

- [CHAR](er-functions-text-char.md)
- [FORMAT](er-functions-text-format.md)
- [LEFT](er-functions-text-left.md)
- [LEN](er-functions-text-len.md)
- [MID](er-functions-text-mid.md)
- [PADLEFT](er-functions-text-padleft.md)
- [REPLACE](er-functions-text-replace.md)
- [RIGHT](er-functions-text-right.md)
- [TEXT](er-functions-text-text.md)
- [TRANSLATE](er-functions-text-translate.md)
- [TRIM](er-functions-text-trim.md)
- [UPPER](er-functions-text-upper.md)

Zie [Lijst met ER-functies van de tekstcategorie](er-functions-category-text.md) voor meer informatie over de transformatie van waarden voor *tekenreeks*.

Een *tekenreeks* kan een onbeperkt aantal tekens bevatten.

Alle vergelijkings [operators](er-formula-language.md#Operators) kunnen worden gebruikt met het gegevenstype *tekenreeks*.

## <a name="additional-resources"></a>Aanvullende bronnen

- [Overzicht van elektronische rapportage](general-electronic-reporting.md)
- [Formuletaal in Elektronische rapportage](er-formula-language.md)
- [Ondersteunde samengestelde gegevenstypen](er-formula-supported-data-types-composite.md)
