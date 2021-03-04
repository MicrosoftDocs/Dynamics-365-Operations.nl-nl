---
title: De ER-functie INTVALUE
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) INTVALUE.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 98b91a983c60bb99280763f7f7a944d08f535e60
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685998"
---
# <a name="intvalue-er-function"></a>De ER-functie INTVALUE

[!include [banner](../includes/banner.md)]

De functie `INTVALUE` retourneert een *Int*-waarde voor de opgegeven tekenreeks.

## <a name="syntax-1"></a>Syntaxis 1

```vb
INTVALUE (text)
```

## <a name="syntax-2"></a>Syntaxis 2

```vb
INTVALUE (number)
```

## <a name="arguments"></a>Argumenten

`text`: *Tekenreeks*

Een tekstwaarde die moet worden geconverteerd naar een *Int*-getal.

`number`: *Werkelijk* of *Geheel getal*

Een numerieke waarde van het type *Werkelijk* of *Geheel getal* die moet worden geconverteerd naar een *Int*-getal.

## <a name="return-values"></a>Retourwaarden

*Int*

De resulterende numerieke waarde.

## <a name="usage-notes"></a>Gebruiksaanwijzingen

Eventuele cijfers achter de komma worden afgekapt.

## <a name="example-1"></a>Voorbeeld 1

`INTVALUE ("100.77")` retourneert de *Int*-waarde **100**.

## <a name="example-2"></a>Voorbeeld 2

`INTVALUE (-100.77)` retourneert de *Int*-waarde **-100**.

## <a name="additional-resources"></a>Aanvullende resources

[Type conversiefuncties](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]