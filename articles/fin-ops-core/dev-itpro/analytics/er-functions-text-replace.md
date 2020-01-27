---
title: De ER-functie REPLACE
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) REPLACE.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: d9c66f4c96f35e3ad5fc92e7925b5cd07c956aac
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916862"
---
# <a name="REPLACE">De ER-functie REPLACE</a>

[!include [banner](../includes/banner.md)]

De functie `REPLACE` retourneert de opgegeven tekenreeks als een waarde van het type *Tekenreeks* nadat deze geheel of gedeeltelijk is vervangen door een andere tekenreeks.

## <a name="syntax"></a>Syntaxis

```
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

Als het argument `regular expression flag` **FALSE**is, gedraagt deze functie zich als [TRANSLATE](er-functions-text-translate.md). De tekens die door het argument `replacement` worden opgegeven, worden gebruikt om de tekens te vervangen die zijn gevonden. 

## <a name="example-1"></a>Voorbeeld 1

`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` past een normale expressie toe waarmee alle niet-numerieke symbolen worden verwijderd en **19234564971** wordt geretourneerd. 

## <a name="example-2"></a>Voorbeeld 2

`REPLACE ("abcdef", "cd", "GH", false)` vervangt het patroon **cd** door de tekenreeks **GH** en retourneert **abGHef**.

## <a name="additional-resources"></a>Aanvullende resources

[Tekstfuncties](er-functions-category-text.md)
