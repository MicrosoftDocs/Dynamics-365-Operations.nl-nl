---
title: De ER-functie ROUND
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) ROUND.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 12af71a024a76fca98fc2e876da9b59e5762cf07
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744546"
---
# <a name="round-er-function"></a>De ER-functie ROUND

[!include [banner](../includes/banner.md)]

De functie `ROUND` retourneert het opgegeven getal als een *werkelijke* waarde nadat deze is afgerond op het opgegeven aantal decimalen.

## <a name="syntax"></a>Syntaxis

```vb
ROUND (number, decimals)
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

Als de waarde van het argument `decimals` hoger is dan 0 (nul), wordt het opgegeven aantal afgerond op dat aantal decimalen.

Als de waarde van het argument `decimals` **0** (nul) is, wordt het opgegeven aantal afgerond op het dichtstbijzijnde hele getal.

Als de waarde van het argument `decimals` minder dan 0 (nul) is, wordt het opgegeven aantal links van de decimale komma afgerond.

## <a name="example-1"></a>Voorbeeld 1

`ROUND (1200.767, 2)` rondt af naar twee decimalen en retourneert **1200,77**.

## <a name="example-2"></a>Voorbeeld 2

`ROUND (1200.767, -3)` rondt af naar het dichtstbijzijnde veelvoud van 1000 en retourneert **1000**.

## <a name="additional-resources"></a>Aanvullende resources

[Wiskundige functies](er-functions-category-mathematical.md)
