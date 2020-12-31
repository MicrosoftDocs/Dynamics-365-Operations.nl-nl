---
title: De ER-functie OR
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) OR.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 107241dbf9a5127d61343fc1cf42c3bab577adb3
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686973"
---
# <a name="or-er-function"></a>De ER-functie OR

[!include [banner](../includes/banner.md)]

De functie `OR` retourneert de *Booleaanse* waarde **FALSE** als alle opgegeven voorwaarden onwaar zijn. De *Booleaanse* waarde **TRUE** wordt geretourneerd als een opgegeven voorwaarde waar is.

## <a name="syntax"></a>Syntaxis

```vb
OR (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a>Argumenten

`condition 1`: *Booleaans*

Een geldige voorwaardelijke expressie die moet worden getest. Dit argument is verplicht.

`condition N`: *Booleaans*

Een geldige voorwaardelijke expressie die moet worden getest. Deze aanvullende argumenten zijn optioneel.

## <a name="return-values"></a>Retourwaarden

*Booleaans*

De resulterende *Booleaanse* waarde.

## <a name="example"></a>Voorbeeld

`OR (1=2, "a"="a")` retourneert **TRUE**.

## <a name="additional-resources"></a>Aanvullende resources

[Logische functies](er-functions-category-logical.md)
