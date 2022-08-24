---
title: De ER-functie INT64VALUE
description: Dit artikel biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) INT64VALUE.
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
ms.openlocfilehash: 4af6cd4ba8b08fe00f53e9dfb1a9156354ec17fc
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292581"
---
# <a name="int64value-er-function"></a>De ER-functie INT64VALUE

[!include [banner](../includes/banner.md)]

De functie `INT64VALUE` retourneert een waarde van het type *Int64* die de opgegeven tekenreeks vertegenwoordigt.

## <a name="syntax-1"></a>Syntaxis 1

```vb
INT64VALUE (text)
```

## <a name="syntax-2"></a>Syntaxis 2

```vb
INT64VALUE (number)
```

## <a name="arguments"></a>Argumenten

`text`: *Tekenreeks*

Een tekstwaarde die moet worden geconverteerd naar een numerieke waarde van het type *Int64*.

`number`: *Werkelijk* of *Geheel getal*

Een numerieke waarde van het type *Werkelijk* of *Geheel getal* die moet worden geconverteerd naar *Int64*.

## <a name="return-values"></a>Retourwaarden

*Int64*

De resulterende numerieke waarde.

## <a name="usage-notes"></a>Gebruiksaanwijzingen

Eventuele cijfers achter de komma worden afgekapt.

## <a name="example-1"></a>Voorbeeld 1

`INT64VALUE ("22565422744")` retourneert de waarde **22565422744** van het type *Int64*.

## <a name="example-2"></a>Voorbeeld 2

`INT64VALUE ( VALUE("22565422744.77"))` retourneert de waarde **22565422744** van het type *Int64*.

## <a name="additional-resources"></a>Aanvullende resources

[Type conversiefuncties](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
