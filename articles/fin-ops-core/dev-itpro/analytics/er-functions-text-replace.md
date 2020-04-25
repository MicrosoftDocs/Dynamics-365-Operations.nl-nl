---
title: De ER-functie REPLACE
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) REPLACE.
author: NickSelin
manager: kfend
ms.date: 04/02/2020
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
ms.openlocfilehash: 83d5095620a938f1ac4b8428fff9209fda7a7831
ms.sourcegitcommit: fb8ad8e2b142441a6530b364f3258bbcc0c724d2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201061"
---
# <a name=""></a><a name="REPLACE">De ER-functie REPLACE</a>

[!include [banner](../includes/banner.md)]

De functie `REPLACE` retourneert de opgegeven tekenreeks als een waarde van het type *Tekenreeks* nadat deze geheel of gedeeltelijk is vervangen door een andere tekenreeks.

## <a name="syntax"></a>Syntaxis

```vb
REPLACE (text, pattern, replacement, regular expression flag)
```

## <a name="arguments"></a>Argumenten

`text`: *Tekenreeks*

Het geldige pad van een gegevensbron van het type *Tekenreeks*.

`pattern`: *Tekenreeks*

Als het argument `regular expression flag` **FALSE** is, bevat dit argument de tekst die moet worden vervangen.

Als het argument `regular expression flag` **TRUE** is, bevat dit argument een reguliere expressie die zowel een zoekpatroon als de vervangende tekst definieert.

`replacement`: *Tekenreeks*

Als het argument `regular expression flag` **FALSE** is, bevat dit argument de tekst die moet worden gebruikt als vervanging.

Als het argument `regular expression flag` **TRUE** is, wordt dit argument niet gebruikt.

`regular expression flag`: *Booleaans*

Een *Booleaanse* waarde die aangeeft of een reguliere expressie wordt gebruikt voor de vervanging.

## <a name="return-values"></a>Retourwaarden

*Tekenreeks*

De resulterende tekstwaarde.

## <a name="usage-notes"></a>Gebruiksaanwijzingen

Als het argument `regular expression flag` **TRUE** is, geeft deze functie als resultaat de opgegeven tekenreeks nadat deze is gewijzigd door de reguliere expressie toe te passen die door het argument `pattern` is opgegeven. De reguliere expressie wordt gebruikt om de tekens te zoeken die moeten worden vervangen.

Als het argument `regular expression flag` **ONWAAR** is, geeft deze functie de opgegeven tekenreeks als resultaat nadat de set tekens die in het argument `pattern` zijn gedefinieerd, is vervangen door tekens van het argument `replacement`. 

## <a name="example-1"></a>Voorbeeld 1

`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` past een normale expressie toe waarmee alle niet-numerieke symbolen worden verwijderd en **19234564971** wordt geretourneerd. 

## <a name="example-2"></a>Voorbeeld 2

`REPLACE ("abcdef", "cd", "GH", false)` vervangt het patroon **cd** door de tekenreeks **GH** en retourneert **abGHef**.

## <a name="additional-resources"></a>Aanvullende resources

[Tekstfuncties](er-functions-category-text.md)
