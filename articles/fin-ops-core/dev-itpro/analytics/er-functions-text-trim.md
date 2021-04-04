---
title: De ER-functie TRIM
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) TRIM.
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
ms.openlocfilehash: b671ef72a3558c17fb16db939770394b225656da
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560031"
---
# <a name="trim-er-function"></a>De ER-functie TRIM

[!include [banner](../includes/banner.md)]

De functie `TRIM` retourneert de opgegeven tekenreeks als een waarde van het type *Tekenreeks* nadat voorloop- en volgspaties zijn afgekapt en nadat meerdere spaties tussen woorden zijn verwijderd.

## <a name="syntax"></a>Syntaxis

```vb
TRIM (text )
```

## <a name="arguments"></a>Argumenten

`text`: *Tekenreeks*

Het geldige pad van een gegevensbron van het type *Tekenreeks*.

## <a name="return-values"></a>Retourwaarden

*Tekenreeks*

De resulterende tekstwaarde.

## <a name="example"></a>Voorbeeld

`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` retourneert **Sample text**.

## <a name="additional-resources"></a>Aanvullende resources

[Tekstfuncties](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]