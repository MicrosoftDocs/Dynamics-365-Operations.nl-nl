---
title: De ER-functie VALUE
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) VALUE.
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 04d3320276bc1e23436bd9baa7a84da36314d6c3bf7f84694aa2e01e31230a0b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6713937"
---
# <a name="value-er-function"></a>De ER-functie VALUE

[!include [banner](../includes/banner.md)]

De functie `VALUE` retourneert een *werkelijke* waarde die is geconverteerd op basis van de opgegeven tekenreeks.

## <a name="syntax"></a>Syntaxis

```vb
VALUE (text)
```

## <a name="arguments"></a>Argumenten

`text`: *Tekenreeks*

Een tekenreekswaarde die moet worden geconverteerd naar een numerieke waarde.

## <a name="return-values"></a>Retourwaarden

*Real-modus*

De resulterende numerieke waarde.

## <a name="usage-notes"></a>Gebruiksaanwijzingen

De komma's en punttekens (.) worden beschouwd als decimale scheidingstekens en er wordt een koppelteken (-) vooraan gebruikt als minteken. Tijdens runtime treedt een uitzondering op als andere niet-numerieke tekens worden aangetroffen in de opgegeven tekenreeks.

## <a name="example-1"></a>Voorbeeld 1

`VALUE ("1 234,56")` leidt tot een uitzondering.

## <a name="example-2"></a>Voorbeeld 2

`VALUE ("1234,56")` retourneert **1234,56**.

## <a name="additional-resources"></a>Aanvullende resources

[Type conversiefuncties](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]