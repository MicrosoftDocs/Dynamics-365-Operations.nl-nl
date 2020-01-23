---
title: De ER-functie TRANSLATE
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) TRANSLATE.
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
ms.openlocfilehash: 11954f3e48d8dc2257b3a0bc8768df47af3c5c0c
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916701"
---
# <a name="TRANSLATE">De ER-functie TRANSLATE</a>

[!include [banner](../includes/banner.md)]

De functie `TRANSLATE` retourneert de opgegeven tekenreeks als een waarde van het type *Tekenreeks* nadat deze geheel of gedeeltelijk is vervangen door een andere tekenreeks.

## <a name="syntax"></a>Syntaxis

```
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a>Argumenten

`text`: *Tekenreeks*

Het geldige pad van een gegevensbron van het type *Tekenreeks*.

`pattern`: *Tekenreeks*

De tekst die moet worden vervangen.

`replacement`: *Tekenreeks*

De tekst die als vervanging moet worden gebruikt.

## <a name="return-values"></a>Retourwaarden

*Tekenreeks*

De resulterende tekstwaarde.

## <a name="example"></a>Voorbeeld

`TRANSLATE ("abcdef", "cd", "GH")` vervangt het patroon **cd** door de tekenreeks **GH** en retourneert **abGHef**.

## <a name="additional-resources"></a>Aanvullende resources

[Tekstfuncties](er-functions-category-text.md)
