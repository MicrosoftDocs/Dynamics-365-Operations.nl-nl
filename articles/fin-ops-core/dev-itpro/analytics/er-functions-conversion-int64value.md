---
title: De ER-functie INT64VALUE
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) INT64VALUE.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
ms.topic: article
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
ms.openlocfilehash: 9db2e9abcac36a8331a494c886218bbfc82e93aa
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561489"
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