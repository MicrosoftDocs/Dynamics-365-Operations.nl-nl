---
title: De ER-functie ABS
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) ABS.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: db12ddddb087556414e81d646c4c87d273a77c133e49152091452d0731916e93
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6776069"
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