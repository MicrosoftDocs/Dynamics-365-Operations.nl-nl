---
title: ER-functie NEWGUID
description: Dit artikel biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) NEWGUID.
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
ms.openlocfilehash: 321e2eda4accf9c8fe33b5a4c092c7be55276f26
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8861811"
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
