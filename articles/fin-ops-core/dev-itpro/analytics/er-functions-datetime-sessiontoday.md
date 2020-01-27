---
title: De ER-functie SESSIONTODAY
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) SESSIONTODAY.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: bcfb36d6e3fb8475546f7cfb420c4aca848ac896
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917460"
---
# <a name="SESSIONTODAY">De ER-functie SESSIONTODAY</a>

[!include [banner](../includes/banner.md)]

De functie `SESSIONTODAY` retourneert een *datumwaarde* die voor de huidige sessiedatum van de toepassingsserver staat.

## <a name="syntax"></a>Syntaxis

```
SESSIONTODAY ()
```

## <a name="return-values"></a>Retourwaarden

*Datum*

De resulterende datumwaarde.

## <a name="example"></a>Voorbeeld

`DATEFORMAT (SESSIONTODAY (), "d", "DE")` retourneert de huidige sessiedatum van de toepassing, 24 december 2015, als de tekenreeks **24-12-2015**, op basis van de geselecteerde Duitse cultuur en de opgegeven notatie.

## <a name="additional-resources"></a>Aanvullende resources

[Datum- en tijdfuncties](er-functions-category-datetime.md)
