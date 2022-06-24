---
title: De ER-functie NUMBERVALUE
description: Dit artikel biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) NUMBERVALUE.
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 9701fe7a1ce2a96fa5fa8df8aeda125c861a117a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871522"
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