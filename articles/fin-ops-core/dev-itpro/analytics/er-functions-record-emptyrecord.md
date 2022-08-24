---
title: ER-functie EMPTYRECORD
description: Dit artikel biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) EMPTYRECORD.
author: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 5046a1cb43f12863ddbdf241e8ba72071d1016ce
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280150"
---
# <a name="emptyrecord-er-function"></a>ER-functie EMPTYRECORD

[!include [banner](../includes/banner.md)]

De functie `EMPTYRECORD` retourneert een nulwaarde voor *Container (record)* met dezelfde structuur als de opgegeven recordlijst of record.

## <a name="syntax"></a>Syntaxis

```vb
EMPTYRECORD (list)
```

## <a name="arguments"></a>Argumenten

`list`: *Recordlijst* of *Container (record)*

Het geldige pad van een gegevensbron van het type *Recordlijst* of *Container (record)*.

## <a name="return-values"></a>Retourwaarden

*Container (record)*

De resulterende recordwaarde.

## <a name="usage-notes"></a>Gebruiksaanwijzingen

> [!NOTE] 
> Een null-record is een record waarin alle velden een lege waarde hebben. Een lege waarde is **0** (nul) voor getallen, een lege tekenreeks voor tekenreeksen, enzovoort.

## <a name="example"></a>Voorbeeld

`EMPTYRECORD (SPLIT ("abc", 1))` retourneert een nieuwe lege record die dezelfde structuur heeft als de lijst die wordt geretourneerd door de functie `SPLIT`. Zie voor meer informatie [SPLIT](er-functions-list-split.md).

## <a name="additional-resources"></a>Aanvullende resources

[Registratiefuncties](er-functions-category-record.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
