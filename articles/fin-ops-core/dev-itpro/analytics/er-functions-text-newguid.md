---
title: ER-functie NEWGUID
description: Dit artikel biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) NEWGUID.
author: kfend
ms.date: 09/09/2021
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-09-08
ms.dyn365.ops.version: AX 10.0.23
ms.custom: ''
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 381dbcbe816c189c1966ffe962020d5aa2b1f3eb
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274767"
---
# <a name="newguid-er-function"></a>ER-functie NEWGUID

[!include [banner](../includes/banner.md)]

Met de functie `NEWGUID` wordt een nieuwe, globaal unieke id (GUID) gegenereerd en als een *[GUID](er-formula-supported-data-types-primitive.md#guid)*-waarde geretourneerd

## <a name="syntax"></a>Syntaxis

```vb
NEWGUID ()
```

## <a name="return-values"></a>Retourwaarden

*GUID*

De resulterende GUID-waarde.

## <a name="example"></a>Voorbeeld

`NEWGUID()` retourneert altijd een nieuwe *GUID*-waarde, zoals **3afcf7ff-af10-ec11-b6e6-000d3a13209e**.

## <a name="additional-resources"></a>Aanvullende bronnen

[Tekstfuncties](er-functions-category-text.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
