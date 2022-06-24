---
title: De ER-functie NUMBERFORMAT
description: Dit artikel biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) NUMBERFORMAT.
author: NickSelin
ms.date: 12/10/2019
ms.prod: ''
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
ms.openlocfilehash: 3e6fa4cbdfb2509418a40980aa29894b5e531bbb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862185"
---
# <a name="numberformat-er-function"></a>De ER-functie NUMBERFORMAT

[!include [banner](../includes/banner.md)]

De functie `NUMBERFORMAT` retourneert een waarde van het type *Tekenreeks* die de opgegeven numerieke waarde in de opgegeven indeling en in een optioneel opgegeven [cultuur](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) bevat. Zie voor informatie over de ondersteunde indelingen [standaard](/dotnet/standard/base-types/standard-numeric-format-strings) en [aangepast](/dotnet/standard/base-types/custom-numeric-format-strings).

## <a name="syntax-1"></a>Syntaxis 1

```vb
NUMBERFORMAT (number, format)
```

## <a name="syntax-2"></a>Syntaxis 2

```vb
NUMBERFORMAT (number, format, culture)
```

## <a name="arguments"></a>Argumenten

`number`: *Geheel getal* of *Werkelijk*

Een numerieke waarde die het getal aangeeft dat moet worden ingedeeld.

`format`: *Tekenreeks*

Een *tekenreekswaarde* die voor de indeling staat.

`culture`: *Tekenreeks*

Een *tekenreekswaarde* die de cultuur vertegenwoordigt die moet worden gebruikt voor de indeling.

## <a name="return-values"></a>Retourwaarden

*Tekenreeks*

De resulterende tekstwaarde.

## <a name="usage-notes"></a>Gebruiksaanwijzingen

Als de cultuur niet is gedefinieerd als een argument van de aangeroepen functie, bepaalt de context waarin deze functie wordt uitgevoerd de cultuur die wordt gebruikt voor het bepalen van de notatie van numerieke waarden.

## <a name="example-1"></a>Voorbeeld 1

Voor de cultuur **EN-US** retourneert `NUMBERFORMAT (0.45, "p")` **10 %** en retourneert `NUMBERFORMAT (10.45, "#")` **10**.

## <a name="example-2"></a>Voorbeeld 2

`NUMBERFORMAT (10/3, "F2", "de")` retourneert **3,33** en `NUMBERFORMAT (10/3, "F2", "en-us")` retourneert **3.33**.

## <a name="additional-resources"></a>Aanvullende resources

[Tekstfuncties](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]