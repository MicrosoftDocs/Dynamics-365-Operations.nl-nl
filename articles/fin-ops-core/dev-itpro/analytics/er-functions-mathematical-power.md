---
title: De ER-functie POWER
description: Dit artikel biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) POWER.
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
ms.openlocfilehash: 9b6693d7c1afebcf9c30d1bf8d72950053c305bd
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273988"
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
