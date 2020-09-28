---
title: De ER-functie NUMBERFORMAT
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) NUMBERFORMAT.
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
ms.openlocfilehash: 8a431414044846bf4e79e6b9f0e5b27281ea8f46
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744402"
---
# <a name="numberformat-er-function"></a>De ER-functie NUMBERFORMAT

[!include [banner](../includes/banner.md)]

De functie `NUMBERFORMAT` retourneert een waarde van het type *Tekenreeks* die de opgegeven numerieke waarde in de opgegeven indeling en in een optioneel opgegeven [cultuur](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) bevat. Zie voor informatie over de ondersteunde indelingen [standaard](https://msdn.microsoft.com/library/dwhawy9k(v=vs.110).aspx) en [aangepast](https://msdn.microsoft.com/library/0c899ak8(v=vs.110).aspx).

## <a name="syntax-1"></a>Syntaxis 1

```vb
NUMBERFORMAT (number, format)
```

## <a name="syntax-2"></a>Syntaxis 2

```vb
NUMBERFORMAT (number, format, culture)
```

## <a name="arguments"></a>Argumenten

`number`: *Geheel getal* of *Werkelijk*

Een numerieke waarde die het getal aangeeft dat moet worden ingedeeld.

`format`: *Tekenreeks*

Een *tekenreekswaarde* die voor de indeling staat.

`culture`: *Tekenreeks*

Een *tekenreekswaarde* die de cultuur vertegenwoordigt die moet worden gebruikt voor de indeling.

## <a name="return-values"></a>Retourwaarden

*Tekenreeks*

De resulterende tekstwaarde.

## <a name="usage-notes"></a>Gebruiksaanwijzingen

Als de cultuur niet is gedefinieerd als een argument van de aangeroepen functie, bepaalt de context waarin deze functie wordt uitgevoerd de cultuur die wordt gebruikt voor het bepalen van de notatie van numerieke waarden.

## <a name="example-1"></a>Voorbeeld 1

Voor de cultuur **EN-US** retourneert `NUMBERFORMAT (0.45, "p")` **10 %** en retourneert `NUMBERFORMAT (10.45, "#")` **10**.

## <a name="example-2"></a>Voorbeeld 2

`NUMBERFORMAT (10/3, "F2", "de")` retourneert **3,33** en `NUMBERFORMAT (10/3, "F2", "en-us")` retourneert **3.33**.

## <a name="additional-resources"></a>Aanvullende resources

[Tekstfuncties](er-functions-category-text.md)
