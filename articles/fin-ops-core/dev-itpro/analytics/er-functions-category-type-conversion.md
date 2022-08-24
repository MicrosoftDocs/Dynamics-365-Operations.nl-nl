---
title: Lijst met ER-functies in de categorie typeconversies
description: Dit artikel biedt informatie over de conversiefuncties die worden ondersteund in ER (Elektronische rapportage).
author: kfend
ms.date: 12/05/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 00fe8c5bce40a59580509a719212f163238815be
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292611"
---
# <a name="list-of-er-functions-in-the-type-conversion-category"></a>Lijst met ER-functies in de categorie typeconversies

[!include [banner](../includes/banner.md)]

ER-typeconversiefuncties kunnen worden gebruikt om waarden tussen typen te converteren. In dit artikel vindt u een overzicht van deze functies.

## <a name="type-conversion-functions"></a>Type conversiefuncties

| Functie | Beschrijving |
|----------|-------------|
| [Int64Value](er-functions-conversion-int64value.md)   | Deze functie retourneert een waarde van het type *Int64* die de opgegeven tekenreeks vertegenwoordigt. |
| [IntValue](er-functions-conversion-intvalue.md)       | Deze functie retourneert een waarde van het type *Int* die de opgegeven tekenreeks vertegenwoordigt. |
| [NumberValue](er-functions-conversion-numbervalue.md) | Deze functie retourneert een *werkelijke* waarde die is geconverteerd op basis van de opgegeven *tekenreekswaarde*. Tijdens de conversie worden de opgegeven scheidingstekens voor decimalen en cijfergroepen in aanmerking genomen. |
| [Waarde](er-functions-conversion-value.md)             | Deze functie retourneert een *werkelijke* waarde die is geconverteerd op basis van de opgegeven *tekenreekswaarde*. |

## <a name="type-conversion-functions-in-the-container-category"></a>Typeconversiefuncties in de containercategorie

In de volgende tabel worden de typeconversiefuncties in de [container](er-functions-category-container.md)categorie beschreven.

| Functie | Beschrijving |
|----------|-------------|
| [Base64StringToContainer](er-functions-container-base64stringtocontainer.md) | Deze functie converteert de opgegeven invoer van het gegevenstype *Tekenreeks* naar een gegevensitem van het gegevenstype *Container*. |

## <a name="type-conversion-functions-in-the-date-and-time-category"></a>Typeconversiefuncties in de datum- en tijdcategorie

In de volgende tabel worden de typeconversiefuncties in de [datum- en tijdcategorie](er-functions-category-datetime.md) beschreven.

| Functie | Beschrijving |
|----------|-------------|
| [DateTimeValue](er-functions-datetime-datetimevalue.md)   | Deze functie retourneert een waarde van het type *DateTime* die van een bepaalde *tekenreekswaarde* in de opgegeven indeling en in een optioneel opgegeven cultuur wordt geconverteerd naar een datum-/tijdwaarde. |
| [DateToDateTime](er-functions-datetime-datetodatetime.md) | Deze functie retourneert een waarde van het type *DateTime* die wordt geconverteerd van een bepaalde *datumwaarde* naar een datum-/tijdwaarde in Coordinated Universal Time (Greenwich Mean Time \[GMT\]). |
| [DateValue](er-functions-datetime-datevalue.md)           | Deze functie retourneert een *datumwaarde* die van een bepaalde *tekenreekswaarde* in de opgegeven indeling en in een optioneel opgegeven cultuur wordt geconverteerd naar een datumwaarde. |

## <a name="type-conversion-functions-in-the-list-category"></a>Typeconversiefuncties in de lijstcategorie

In de volgende tabel worden de typeconversiefuncties in de [lijstcategorie](er-functions-category-list.md) beschreven.

| Functie | Beschrijving |
|----------|-------------|
| [Weergeven](er-functions-list-list.md)                 | Deze functie retourneert een waarde van het type *Recordlijst* als een nieuwe lijst die wordt gemaakt op basis van opgegeven argumenten van het type *Container (record)*. |
| [ListOfFields](er-functions-list-listoffields.md) | Deze functie retourneert een *recordlijstwaarde* die wordt gemaakt op basis van de structuur een bepaald argument van het type *Opsomming* of *Container (record)*. |
| [Splitsen](er-functions-list-split.md)               | Deze functie splitst de opgegeven *tekenreekswaarde* in subtekenreeksen en retourneert het resultaat als een nieuwe waarde van het type *Recordlijst*. |
| [StringJoin](er-functions-list-stringjoin.md)     | Deze functie retourneert een *tekenreekswaarde* die bestaat uit samengevoegde waarden van het opgegeven veld op basis van de opgegeven *recordlijstwaarde*. De waarden kunnen worden gescheiden door het opgegeven scheidingsteken. |

## <a name="type-conversion-functions-in-the-text-category"></a>Typeconversiefuncties in de tekstcategorie

In de volgende tabel worden de typeconversiefuncties in de [tekstcategorie](er-functions-category-text.md) beschreven.

| Functie | Beschrijving |
|----------|-------------|
| [Char](er-functions-text-char.md)                 | Deze functie retourneert een waarde van het type *Tekenreeks* van één teken waarnaar wordt verwezen door het opgegeven Unicode-nummer. |
| [GuidValue](er-functions-text-guidvalue.md)       | Deze functie converteert de opgegeven invoer van het gegevenstype *Tekenreeks* naar een gegevensitem van het gegevenstype *GUID*. |
| [NumberFormat](er-functions-text-numberformat.md) | Deze functie retourneert een *tekenreekswaarde* die de opgegeven numerieke waarde in de opgegeven indeling en in een optioneel opgegeven cultuur bevat. |
| [QrCode](er-functions-text-qrcode.md)             | Deze functie retourneert een waarde van het type *Container* die afbeelding met de QR-code (Quick Response) voor de opgegeven tekenreeks in binaire indeling weergeeft. |
| [Tekst](er-functions-text-text.md)                 | Deze functie retourneert een *tekenreekswaarde* voor de opgegeven numerieke waarde nadat deze is geconverteerd naar een tekenreeks die wordt opgemaakt volgens de lokale instellingen van de server van het huidige exemplaar. |

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht van elektronische rapportage](general-electronic-reporting.md)

[Formuleontwerper in elektronische aangifte](general-electronic-reporting-formula-designer.md)

[Formuletaal in Elektronische rapportage](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
