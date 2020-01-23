---
title: De ER-functie SESSIONNOW
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) SESSIONNOW.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4dff6daa8fbd60ef1fc84d783e428d69477aac6d
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916264"
---
# <a name="">De ER-functie SESSIONNOW</a>

[!include [banner](../includes/banner.md)]

De functie `SESSIONNOW` retourneert een waarde van het type *DateTime* die voor de huidige sessiedatum en -tijd van de toepassingsserver staat.

## <a name="syntax"></a>Syntaxis

```
SESSIONNOW ()
```

## <a name="return-values"></a>Retourwaarden

*Datum/tijd*

De resulterende datum-/tijdwaarde.

## <a name="example"></a>Voorbeeld

`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` retourneert de huidige sessiedatum/-tijd van de toepassing, 24 december 2015, als **24.12.2015**, op basis van de geselecteerde Duitse cultuur en de opgegeven notatie.

## <a name="additional-resources"></a>Aanvullende resources

[Datum- en tijdfuncties](er-functions-category-datetime.md)
