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
ms.openlocfilehash: 392135abaf7db05d5ac591ab56312a0e0f6ae5ff
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916793"
---
# <a name="NUMBERFORMAT">De ER-functie NUMBERFORMAT</a>

[!include [banner](../includes/banner.md)]

De functie `NUMBERFORMAT` retourneert een waarde van het type *Tekenreeks* die de opgegeven numerieke waarde in de opgegeven indeling en in een optioneel opgegeven [cultuur](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) bevat. Zie voor informatie over de ondersteunde indelingen [standaard](https://msdn.microsoft.com/library/dwhawy9k(v=vs.110).aspx) en [aangepast](https://msdn.microsoft.com/library/0c899ak8(v=vs.110).aspx).

## <a name="syntax-1"></a>Syntaxis 1

```
NUMBERFORMAT (number, format)
```

## <a name="syntax-2"></a>Syntaxis 2

```
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
