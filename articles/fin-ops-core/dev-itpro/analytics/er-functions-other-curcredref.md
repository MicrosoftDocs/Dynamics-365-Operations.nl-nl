---
title: De ER-functie CURCREDREF
description: Dit artikel biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) CURCREDREF.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: 28651a4c238fd56625700ccb6a2a9d73aa23e8d7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901588"
---
# <a name="curcredref-er-function"></a>De ER-functie CURCREDREF

[!include [banner](../includes/banner.md)]

De functie `CURCREDREF` retourneert een *tekenreekswaarde* voor een crediteurverwijzing, op basis van de cijfers van het opgegeven factuurnummer.

## <a name="syntax"></a>Syntaxis

```vb
CURCREDREF (invoice number digits)
```

## <a name="arguments"></a>Argumenten

`invoice number digits`: *Tekenreeks*

Een tekstwaarde die voor de cijfers van een factuurnummer staat.

## <a name="return-values"></a>Retourwaarden

*Tekenreeks*

De resulterende tekstwaarde.

## <a name="example"></a>Voorbeeld

`CURCredRef ("VEND-200002")` retourneert **2200002**.

## <a name="additional-resources"></a>Aanvullende resources

[Andere functies (voor specifiek zakelijk domein)](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]