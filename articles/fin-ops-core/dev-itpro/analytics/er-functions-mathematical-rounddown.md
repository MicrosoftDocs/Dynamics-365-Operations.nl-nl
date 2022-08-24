---
title: De ER-functie ROUNDDOWN
description: Dit artikel biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) ROUNDDOWN.
author: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: e0fa2c92fe63c3c89548b5cc23dd714d3d7589af
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286084"
---
# <a name="rounddown-er-function"></a>De ER-functie ROUNDDOWN

[!include [banner](../includes/banner.md)]

De functie `ROUNDDOWN` retourneert het opgegeven getal als een *werkelijke* waarde nadat deze naar beneden is afgerond op het opgegeven aantal decimalen.

## <a name="syntax"></a>Syntaxis

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a>Argumenten

`number`: *Werkelijk*

Een numerieke waarde die moet worden afgerond.

`decimals`: *Geheel getal*

Een numerieke waarde die het aantal decimalen aangeeft.

## <a name="return-values"></a>Retourwaarden

*Real-modus*

De resulterende numerieke waarde.

## <a name="usage-notes"></a>Gebruiksaanwijzingen

Deze functie werkt als [ROUND](er-functions-mathematical-round.md), maar rondt altijd het opgegeven getal naar beneden af (richting nul).

## <a name="example-1"></a>Voorbeeld 1

`ROUNDDOWN (1200.767, 2)` rondt naar beneden af op twee decimalen en retourneert **1200,76**. 

## <a name="example-2"></a>Voorbeeld 2

`ROUNDDOWN (1700.767, -3)` rondt naar beneden af naar het dichtstbijzijnde veelvoud van 1000 en retourneert **1000**.

## <a name="additional-resources"></a>Aanvullende resources

[Wiskundige functies](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
