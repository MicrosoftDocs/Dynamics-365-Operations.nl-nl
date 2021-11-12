---
title: ER-functie NEWGUID
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) NEWGUID.
author: NickSelin
ms.date: 09/09/2021
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-09-08
ms.dyn365.ops.version: AX 10.0.23
ms.openlocfilehash: 5856a4d765f5136ecb11a34e0255c1ba88818f2c
ms.sourcegitcommit: 9e8d7536de7e1f01a3a707589f5cd8ca478d657b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/18/2021
ms.locfileid: "7647928"
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
