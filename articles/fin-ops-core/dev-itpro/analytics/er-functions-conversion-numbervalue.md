---
title: De ER-functie NUMBERVALUE
description: Dit artikel biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) NUMBERVALUE.
author: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 2e39cf59cabd44583e78ff2c35a7ae4d6edbd7ee
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282586"
---
# <a name="numbervalue-er-function"></a>De ER-functie NUMBERVALUE

[!include [banner](../includes/banner.md)]

De functie `NUMBERVALUE` retourneert een *werkelijke* waarde die is geconverteerd op basis van de opgegeven *tekenreekswaarde*. Tijdens de conversie worden de opgegeven scheidingstekens voor decimalen en cijfergroepen in aanmerking genomen.

## <a name="syntax"></a>Syntaxis

```vb
NUMBERVALUE (text, decimal separator, digit grouping separator)
```

## <a name="arguments"></a>Argumenten

`text`: *Tekenreeks*

Een tekstwaarde die moet worden geconverteerd naar een *werkelijk* getal.

`decimal separator`: Tekenreeks

Een decimaalteken. Dit wordt gebruikt om het gehele getal en de breukdelen van een decimaal getal te scheiden.

`digit grouping separator`: *Tekenreeks*

Een scheidingsteken voor het groeperen van cijfers. Deze wordt gebruikt als het scheidingsteken voor duizendtallen.

## <a name="return-values"></a>Retourwaarden

*Real-modus*

De resulterende numerieke waarde.

## <a name="example"></a>Voorbeeld

`NUMBERVALUE( "1 234,56", ",", " ")` retourneert **1234,56**.

## <a name="additional-resources"></a>Aanvullende resources

[Type conversiefuncties](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
