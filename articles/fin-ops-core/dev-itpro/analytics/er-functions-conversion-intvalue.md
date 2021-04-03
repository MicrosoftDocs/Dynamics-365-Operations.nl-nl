---
title: De ER-functie INTVALUE
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) INTVALUE.
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
ms.openlocfilehash: 64f43ad29d59ade1e124b6800734b003f6ca07df
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561465"
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