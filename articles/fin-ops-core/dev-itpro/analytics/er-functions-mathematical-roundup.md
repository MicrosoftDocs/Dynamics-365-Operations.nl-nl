---
title: De ER-functie ROUNDUP
description: Dit artikel biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) ROUNDUP.
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
ms.openlocfilehash: ec4fdce6f072c5c3d87b139c8f64bd63a8a3eccd
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855640"
---
# <a name="roundup-er-function"></a>De ER-functie ROUNDUP

[!include [banner](../includes/banner.md)]

De functie `ROUNDUP` retourneert het opgegeven getal als een *werkelijke* waarde nadat deze omhoog is afgerond op het opgegeven aantal decimalen.

## <a name="syntax"></a>Syntaxis

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a>Argumenten

`number`: *Werkelijk*

Een numerieke waarde die omhoog moet worden afgerond.

`decimals`: *Geheel getal*

Een numerieke waarde die het aantal decimalen aangeeft.

## <a name="return-values"></a>Retourwaarden

*Real-modus*

De resulterende numerieke waarde.

## <a name="usage-notes"></a>Gebruiksaanwijzingen

Deze functie werkt als [ROUND](er-functions-mathematical-round.md), maar rondt altijd het opgegeven getal naar boven af (weg van nul).

## <a name="example-1"></a>Voorbeeld 1

`ROUNDUP (1200.763, 2)` rondt omhoog af naar twee decimalen en retourneert **1200,77**.

## <a name="example-2"></a>Voorbeeld 2

`ROUNDUP (1200.767, -3)` rondt omhoog af naar het dichtstbijzijnde veelvoud van 1000 en retourneert **2000**.

## <a name="additional-resources"></a>Aanvullende resources

[Wiskundige functies](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]