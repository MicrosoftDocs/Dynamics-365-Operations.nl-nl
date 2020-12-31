---
title: De ER-functie POWER
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) POWER.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 858f59cf0bc6387b09cbb6f0c59f58ba8107582c
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683324"
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
