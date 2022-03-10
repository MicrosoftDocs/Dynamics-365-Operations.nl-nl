---
title: De ER-functie POWER
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) POWER.
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
ms.openlocfilehash: 6955d2787b2a9be6d38fe10165a9d5ef8310b108e3a9772709d9d1ff51712424
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6767139"
---
# <a name="power-er-function"></a>De ER-functie POWER

[!include [banner](../includes/banner.md)]

De functie `POWER` retourneert een *werkelijke* waarde die het resultaat vertegenwoordigt van het verheffen van het opgegeven positieve getal naar de opgegeven macht.

## <a name="syntax"></a>Syntaxis

```vb
POWER (number, power)
```

## <a name="arguments"></a>Argumenten

`number`: *Werkelijk* of *Geheel getal*

Een numerieke waarde die moet worden verheven naar de opgegeven macht.

`power`: *Werkelijk* of *Geheel getal*

Een numerieke waarde die de specifieke macht vertegenwoordigt.

## <a name="return-values"></a>Retourwaarden

*Real-modus*

De resulterende numerieke waarde.

## <a name="example-1"></a>Voorbeeld 1

`POWER (10, 2)` retourneert **100**.

## <a name="example-2"></a>Voorbeeld 2

`POWER (4, 0.5)` retourneert **2**.

## <a name="additional-resources"></a>Aanvullende resources

[Wiskundige functies](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]