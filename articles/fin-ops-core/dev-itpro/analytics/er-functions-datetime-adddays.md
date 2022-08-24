---
title: De ER-functie ADDDAYS
description: Dit artikel biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) ADDDAYS.
author: kfend
ms.date: 12/03/2019
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
ms.openlocfilehash: 69273794def0dc52dc8e31615c319ccf5067fa77
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274134"
---
# <a name="adddays-er-function"></a>De ER-functie ADDDAYS

[!include [banner](../includes/banner.md)]

De functie `ADDDAYS` berekent een waarde van het type *DateTime* voor het opgegeven aantal dagen vóór of na een opgegeven begindatum.

## <a name="syntax"></a>Syntaxis

```vb
ADDDAYS (datetime, days)
```

## <a name="arguments"></a>Argumenten

`datetime`: *DateTime*

Een datum-/tijdwaarde voor de begindatum.

`days`: *Geheel getal*

Het aantal dagen voor of na `datetime`.

## <a name="return-values"></a>Retourwaarden

*Datum/tijd*

De resulterende datum-/tijdwaarde.

## <a name="usage-notes"></a>Gebruiksaanwijzingen

Een positieve waarde voor `days` levert een toekomstige datum op. Een negatieve waarde resulteert in een datum in het verleden.

## <a name="example-1"></a>Voorbeeld 1

`ADDDAYS (NOW(), 7)` retourneert de datum en tijd over zeven dagen.

## <a name="example-2"></a>Voorbeeld 2

`ADDDAYS (NOW(), -3)` retourneert de datum en tijd van drie dagen geleden.

## <a name="additional-resources"></a>Aanvullende resources

[Datum- en tijdfuncties](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
