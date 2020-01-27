---
title: Lijst met ER-functies in de datum- en tijdcategorie
description: Dit onderwerp biedt informatie over de datum- en tijdfuncties die worden ondersteund in ER (Elektronische rapportage).
author: NickSelin
manager: kfend
ms.date: 12/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fa8e725ac6bd7d280dc0269a70e3f7abf1ad4d43
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916563"
---
# <a name="list-of-er-functions-in-the-date-and-time-category"></a>Lijst met ER-functies in de datum- en tijdcategorie

[!include [banner](../includes/banner.md)]

Datum- en tijdfuncties in ER kunnen worden gebruikt om informatie te extraheren uit datum- en tijdwaarden en om hierop bewerkingen uit te voeren. In dit onderwerp vindt u een overzicht van deze functies.

## <a name="list-of-supported-functions"></a>Lijst met ondersteunde functies

| Functie | Beschrijving |
|----------|-------------|
| [AddDays](er-functions-datetime-adddays.md) | Deze functie retourneert een waarde van het type *DateTime* voor het opgegeven aantal dagen vóór of na een opgegeven begindatum. |
| [DateFormat](er-functions-datetime-dateformat.md) | Deze functie retourneert een waarde van het type *Tekenreeks* voor een bepaalde datumwaarde als tekst in de opgegeven indeling en in een optioneel opgegeven cultuur. |
| [DateTimeFormat](er-functions-datetime-datetimeformat.md) | Deze functie retourneert een waarde van het type *Tekenreeks* voor een bepaalde datum-/tijdwaarde als tekst in de opgegeven indeling en in een optioneel opgegeven cultuur. |
| [DateTimeValue](er-functions-datetime-datetimevalue.md) | Deze functie retourneert een waarde van het type *DateTime* die van een bepaalde tekstwaarde in de opgegeven indeling en in een optioneel opgegeven cultuur wordt geconverteerd naar een datum-/tijdwaarde. |
| [DateToDateTime](er-functions-datetime-datetodatetime.md) | Deze functie retourneert een waarde van het type *DateTime* die wordt geconverteerd van een bepaalde datumwaarde naar een datum-/tijdwaarde in Coordinated Universal Time (Greenwich Mean Time \[GMT\]). |
| [DateValue](er-functions-datetime-datevalue.md) | Deze functie retourneert een *datumwaarde* die van een bepaalde tekstwaarde in de opgegeven indeling en in een optioneel opgegeven cultuur wordt geconverteerd naar een datumwaarde. |
| [DayOfYear](er-functions-datetime-dayofyear.md) | Deze functie retourneert een *geheel getal* dat staat voor het aantal dagen tussen 1 januari en de opgegeven datum. |
| [Dagen](er-functions-datetime-days.md) | Deze functie retourneert een *geheel getal* dat staat voor het aantal dagen tussen de ene en een andere opgegeven datum. |
| [Now](er-functions-datetime-now.md) | Deze functie retourneert een waarde van het type *DateTime* die voor de huidige datum en tijd van de toepassingsserver staat. |
| [NullDate](er-functions-datetime-nulldate.md) | Deze functie retourneert een *datumwaarde* die voor de **nuldatum** staat (1 januari 1900). |
| [NullDateTime](er-functions-datetime-nulldatetime.md) | Deze functie retourneert een waarde van het type *DateTime* die voor de **nuldatum en -tijd** staat (1 januari 1900) in Coordinated Universal Time. |
| [SessionNow](er-functions-datetime-sessionnow.md) | Deze functie retourneert een waarde van het type *DateTime* die voor de huidige sessiedatum en -tijd van de toepassingsserver staat. |
| [SessionToday](er-functions-datetime-sessiontoday.md) | Deze functie retourneert een *datumwaarde* die voor de huidige sessiedatum van de toepassingsserver staat. |
| [Vandaag](er-functions-datetime-today.md) | Deze functie retourneert een *datumwaarde* die voor de huidige datum van de toepassingsserver staat. |

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht van elektronische rapportage](general-electronic-reporting.md)

[Formuleontwerper in elektronische aangifte](general-electronic-reporting-formula-designer.md)

[Formuletaal in Elektronische rapportage](er-formula-language.md)
