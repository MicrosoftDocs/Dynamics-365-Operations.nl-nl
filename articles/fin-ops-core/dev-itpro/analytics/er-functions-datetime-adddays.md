---
title: De ER-functie ADDDAYS
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) ADDDAYS.
author: NickSelin
ms.date: 12/03/2019
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
ms.openlocfilehash: 0c420daa04b8e22504d25d317c75826f1d1914b7
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747054"
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