---
title: De ER-functie DAYOFYEAR
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) DAYOFYEAR.
author: NickSelin
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
ms.openlocfilehash: 569e988db91ff992fb7db6e7fd6e8c6aa6a1a3e8
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746910"
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