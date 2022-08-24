---
title: De ER-functie ABS
description: Dit artikel biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) ABS.
author: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: a8d0fe68232d9dd27d9ba0cc6b81c7708d22711e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272553"
---
# <a name="abs-er-function"></a>De ER-functie ABS

[!include [banner](../includes/banner.md)]

De functie `ABS` retourneert de absolute waarde (modulus) van de opgegeven numerieke waarde als een *werkelijke* waarde. Met andere woorden, het getal wordt zonder teken geretourneerd.

## <a name="syntax"></a>Syntaxis

```vb
ABS (number)
```

## <a name="arguments"></a>Argumenten

`number`: *Werkelijk*

Een numerieke waarde waarvan u de modulus wilt.

## <a name="return-values"></a>Retourwaarden

*Real-modus*

De resulterende numerieke waarde.

## <a name="example"></a>Voorbeeld

`ABS (-1)` retourneert **1**.

## <a name="additional-resources"></a>Aanvullende resources

[Wiskundige functies](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
