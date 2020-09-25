---
title: De ER-functie PADLEFT
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) PADLEFT.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 3f8a8e2006fe279b25bbf154c6e1802babf51117
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744354"
---
# <a name="padleft-er-function"></a>De ER-functie PADLEFT

[!include [banner](../includes/banner.md)]

De functie `PADLEFT` retourneert een *tekenreeks* met de opgegeven lengte waarbij het begin van de opgegeven tekenreeks is aangevuld met de opgegeven tekens.

## <a name="syntax"></a>Syntaxis

```vb
PADLEFT (text, length, padding chars)
```

## <a name="arguments"></a>Argumenten

`text`: *Tekenreeks*

Een *tekenreekswaarde* die voor de oorspronkelijke tekst staat.

`length`: *Geheel getal*

Een *geheel getal* dat voor het uiteindelijke aantal tekens in de aangevulde tekenreeks staat.

`padding chars`: *Tekenreeks*

De tekens die moeten worden gebruikt voor opvulling.

## <a name="return-values"></a>Retourwaarden

*Tekenreeks*

De resulterende tekstwaarde.

## <a name="example"></a>Voorbeeld

`PADLEFT ("1234", 10, "`&nbsp;`")` retourneert de tekenreeks **&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234**.

## <a name="additional-resources"></a>Aanvullende resources

[Tekstfuncties](er-functions-category-text.md)
