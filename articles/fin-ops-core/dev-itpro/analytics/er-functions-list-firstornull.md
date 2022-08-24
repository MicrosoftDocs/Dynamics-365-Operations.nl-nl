---
title: De ER-functie FIRSTORNULL
description: In dit artikel wordt uitgelegd hoe de ER-functie (Elektronische rapportage) FIRSTORNULL wordt gebruikt.
author: kfend
ms.date: 11/29/2019
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
ms.openlocfilehash: 7ee1a5c1b6ac13581608f9adbda42fae0706d225
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273183"
---
# <a name="firstornull-er-function"></a>De ER-functie FIRSTORNULL

[!include [banner](../includes/banner.md)]

De functie `FIRSTORNULL` retourneert de eerste record van de opgegeven lijst als een waarde van het type *Container (record)*, als die record niet leeg is. Als de record leeg is, retourneert deze functie een nulwaarde voor *Container (record)*.

## <a name="syntax"></a>Syntaxis

```vb
FIRSTORNULL (list)
```

## <a name="arguments"></a>Argumenten

`list`: *Recordlijst*

Het geldige pad van een gegevensbron van het gegevenstype *Recordlijst*.

## <a name="return-values"></a>Retourwaarden

*Container (record)*

De resulterende recordwaarde.

## <a name="example"></a>Voorbeeld

De expressie `FIRSTORNULL(SPLIT("",1)).Value` retourneert een lege tekenreeks (**""**).

## <a name="additional-resources"></a>Aanvullende resources

[Lijstfuncties](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
