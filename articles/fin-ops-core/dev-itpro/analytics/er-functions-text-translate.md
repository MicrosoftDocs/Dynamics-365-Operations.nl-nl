---
title: De ER-functie TRANSLATE
description: Dit artikel biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) TRANSLATE.
author: kfend
ms.date: 04/02/2020
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
ms.openlocfilehash: 7a15a28f6efa5333b54aa34938d22a9d6e404cec
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278436"
---
# <a name="translate-er-function"></a>De ER-functie TRANSLATE

[!include [banner](../includes/banner.md)]

De functie `TRANSLATE` retourneert een waarde voor een *Tekenreeks* die het resultaat bevat van de vervanging van de opgegeven tekst in tekens van een andere opgegeven set.

## <a name="syntax"></a>Syntaxis

```vb
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a>Argumenten

`text`: *Tekenreeks*

Het geldige pad van een gegevensbron van het type *Tekenreeks*.

`pattern`: *Tekenreeks*

De tekst die moet worden vervangen.

`replacement`: *Tekenreeks*

De tekst die als vervanging moet worden gebruikt.

## <a name="return-values"></a>Retourwaarden

*Tekenreeks*

De resulterende tekstwaarde.

## <a name="usage-notes"></a>Gebruiksaanwijzingen

De functie `TRANSLATE` vervangt één teken per keer. Het eerste teken van het argument `text` wordt vervangen door het eerste teken van het argument `pattern`. Daarna volgt het tweede teken en wordt dezelfde stroom gebruikt totdat de taak is voltooid. Wanneer een teken van de argumenten `text` en `pattern` overeenkomt, wordt het vervangen door een teken uit het argument `replacement` dat zich op dezelfde positie bevindt als het teken uit het argument `pattern`. Als een teken meerdere keren voorkomt in het argument `pattern`, wordt de argumenttoewijzing `replacement` gebruikt die overeenkomt met de eerste instantie van dit teken.

## <a name="example-1"></a>Voorbeeld 1

`TRANSLATE ("abcdef", "cd", "GH")` vervangt het teken **"c"** van de opgegeven tekst **"abcdef"** door het teken **"G** " van de tekst `replacement` omdat:
-   Het teken **"c"** wordt weergegeven in de tekst `pattern` op de eerste positie.
-   De eerste positie van de tekst `replacement` bevat het teken **"G"**.

## <a name="example-2"></a>Voorbeeld 2

`TRANSLATE ("abcdef", "ccd", "GH")` retourneert **"abGdef"**.

## <a name="example-3"></a>Voorbeeld 3

`TRANSLATE ("abccba", "abc", "123")` retourneert **123321**.

## <a name="additional-resources"></a>Aanvullende bronnen

[Tekstfuncties](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
