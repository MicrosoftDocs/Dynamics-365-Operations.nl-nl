---
title: Lijst met ER-functies van de tekstcategorie
description: Dit onderwerp biedt informatie over de tekstfuncties die worden ondersteund in ER (Elektronische rapportage).
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
ms.openlocfilehash: f519d242fe74196b0d12bdc9df4f1b4b0e585752
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916609"
---
# <a name="list-of-er-functions-of-the-text-category"></a>Lijst met ER-functies van de tekstcategorie

[!include [banner](../includes/banner.md)]

ER-tekstfuncties kunnen worden gebruikt om bewerkingen uit te voeren op gegevensbronnen van het gegevenstype *Tekenreeks*. In dit onderwerp vindt u een overzicht van deze functies.

## <a name="list-of-supported-functions"></a>Lijst met ondersteunde functies

| Functie | Beschrijving |
|----------|-------------|
| [Char](er-functions-text-char.md) | Deze functie retourneert een waarde van het type *Tekenreeks* van één teken waarnaar wordt verwezen door het opgegeven Unicode-nummer. |
| [Samenvoegen](er-functions-text-concatenate.md) | Deze functie retourneert alle opgegeven tekenreeksen als een waarde van het type *Tekenreeks* nadat ze zijn samengevoegd in één tekenreeks. |
| [Indeling](er-functions-text-format.md) | Met deze functie retourneert de opgegeven tekenreeks een waarde van het type *Tekenreeks* nadat deze is ingedeeld door elk exemplaar van **%N** te vervangen door het *N*e argument. |
| [GetEnumValueByName](er-functions-text-getenumvaluebyname.md) | Deze functie zoekt naar een specifieke waarde van het type *Opsomming* in de opgegeven gegevensbron voor opsommingen met behulp van de opsommingsnaam die is opgegeven als waarde van het type *Tekenreeks*. Als de waarde van het type *Opsomming* wordt gevonden, wordt deze geretourneerd. |
| [GuidValue](er-functions-text-guidvalue.md) | Deze functie converteert de opgegeven invoer van het gegevenstype *Tekenreeks* naar een gegevensitem van het gegevenstype *GUID*. |
| [JsonValue](er-functions-text-jsonvalue.md) | Deze functie parseert gegevens in de indeling JavaScript Object Notation (JSON), die kan worden geopend op het opgegeven pad, en er wordt een scalaire waarde geëxtraheerd die is gebaseerd op de opgegeven id. Vervolgens wordt de geëxtraheerde scalaire waarde als een *tekenreekswaarde* geretourneerd. |
| [Links](er-functions-text-left.md) | Deze functie retourneert een waarde van het type *Tekenreeks* die het opgegeven aantal tekens vanaf het begin van de opgegeven tekenreeks bevat. |
| [Len](er-functions-text-len.md) | Deze functie retourneert een waarde van het type *Geheel getal* die het opgegeven aantal tekens in de opgegeven tekenreeks bevat. |
| [Lower](er-functions-text-lower.md) | Deze functie retourneert de opgegeven tekstreeks als een waarde van het type *Tekenreeks* nadat deze is geconverteerd naar kleine letters. |
| [Mid](er-functions-text-mid.md) | Deze functie retourneert een waarde van het type *Tekenreeks* die het opgegeven aantal tekens vanaf de opgegeven positie van de opgegeven tekenreeks bevat. |
| [NumberFormat](er-functions-text-numberformat.md) | Deze functie retourneert een waarde van het type *Tekenreeks* die de opgegeven numerieke waarde in de opgegeven indeling en in een optioneel opgegeven cultuur bevat. |
| [NumeralsToText](er-functions-text-numeralstotext.md) | Deze functie retourneert de opgegeven numerieke waarde als een waarde van het type *Tekenreeks* nadat deze is gespeld (geconverteerd naar tekstreeksen) in de opgegeven taal. |
| [PadLeft](er-functions-text-padleft.md) | Deze functie retourneert een waarde van het type *Tekenreeks* met de opgegeven lengte, waarbij het begin van de opgegeven tekenreeks wordt aangevuld met een of meer van de opgegeven tekens. |
| [QrCode](er-functions-text-qrcode.md) | Deze functie retourneert een waarde van het type *Container* die afbeelding met de QR-code (Quick Response) voor de opgegeven tekenreeks in binaire indeling weergeeft. |
| [Vervangen](er-functions-text-replace.md) | Deze functie retourneert de opgegeven tekenreeks als een waarde van het type *Tekenreeks* nadat deze geheel of gedeeltelijk is vervangen door een andere tekenreeks. |
| [Rechts](er-functions-text-right.md) | Deze functie retourneert een waarde van het type *Tekenreeks* die het opgegeven aantal tekens vanaf het einde van de opgegeven tekenreeks bevat. |
| [Tekst](er-functions-text-text.md) | Deze functie retourneert de opgegeven numerieke waarde als een waarde van het type *Tekenreeks* nadat deze is geconverteerd naar een tekenreeks die wordt opgemaakt volgens de lokale instellingen van de server van het huidige exemplaar. |
| [Vertalen](er-functions-text-translate.md) | Deze functie retourneert de opgegeven tekenreeks als een waarde van het type *Tekenreeks* nadat deze geheel of gedeeltelijk is vervangen door een andere tekenreeks. |
| [Trim](er-functions-text-trim.md) | Deze functie retourneert de opgegeven tekenreeks als een waarde van het type *Tekenreeks* nadat voorloop- en volgspaties zijn afgekapt en nadat meerdere spaties tussen woorden zijn verwijderd. |
| [Upper](er-functions-text-upper.md) | Deze functie retourneert de opgegeven tekstreeks als een waarde van het type *Tekenreeks* nadat deze is geconverteerd naar hoofdletters. |

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht van elektronische rapportage](general-electronic-reporting.md)

[Formuleontwerper in elektronische aangifte](general-electronic-reporting-formula-designer.md)

[Formuletaal in Elektronische rapportage](er-formula-language.md)
