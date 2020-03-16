---
title: De ER-functie MOD_97
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) MOD_97.
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
ms.openlocfilehash: ce2192c7bc849996e08573d71d8ed43956c8fb89
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070524"
---
# <a name="MOD_97">De ER-functie MOD_97</a>

[!include [banner](../includes/banner.md)]

De functie `MOD_97` retourneert een *tekenreekswaarde* voor een crediteurverwijzing als een MOD97-expressie, op basis van de cijfers van het opgegeven factuurnummer.

## <a name="syntax"></a>Syntaxis

```vb
MOD_97 (invoice number digits)
```

## <a name="arguments"></a>Argumenten

`invoice number digits`: *Tekenreeks*

Een tekstwaarde die voor de cijfers van een factuurnummer staat.

## <a name="return-values"></a>Retourwaarden

*Tekenreeks*

De resulterende tekstwaarde.

## <a name="example"></a>Voorbeeld

`MOD_97 ("VEND-200002")` retourneert **20000285**.

## <a name="additional-resources"></a>Aanvullende resources

[Andere functies (voor specifiek zakelijk domein)](er-functions-category-other.md)
