---
title: De ER-functie VALUE
description: Dit artikel biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) VALUE.
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
ms.openlocfilehash: 0a47637c47ca6c947451efa1230191779401b4e1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277657"
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
