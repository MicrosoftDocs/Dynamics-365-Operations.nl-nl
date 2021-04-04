---
title: De ER-functie DAYOFYEAR
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) DAYOFYEAR.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: ba63c96355a6a7a1eccaddf39e47a3edb2d1e651
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563529"
---
# <a name="dayofyear-er-function"></a>De ER-functie DAYOFYEAR

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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]