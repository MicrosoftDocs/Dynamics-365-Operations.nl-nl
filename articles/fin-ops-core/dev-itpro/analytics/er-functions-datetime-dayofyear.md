---
title: De ER-functie DAYOFYEAR
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) DAYOFYEAR.
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
ms.openlocfilehash: d24aabb582151b0b357b64a988cc932a9c9f3cea
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070662"
---
# <a name="DAYOFYEAR">De ER-functie DAYOFYEAR</a>

[!include [banner](../includes/banner.md)]

De functie `DAYOFYEAR` retourneert een *geheel getal* dat staat voor het aantal dagen tussen 1 januari en de opgegeven datum.

## <a name="syntax"></a>Syntaxis

```vb
DAYOFYEAR (date) as Integer
```

## <a name="arguments"></a>Argumenten

`date`: *Datum*

Een datumwaarde die de begindatum voor de berekening van het aantal dagen vertegenwoordigt.

## <a name="return-values"></a>Retourwaarden

*Geheel getal*

De resulterende numerieke waarde.

## <a name="example-1"></a>Voorbeeld 1

`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` retourneert **61**.

## <a name="example-2"></a>Voorbeeld 2

`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` retourneert **1**.

## <a name="additional-resources"></a>Aanvullende resources

[Datum- en tijdfuncties](er-functions-category-datetime.md)
