---
title: De ER-functie INTVALUE
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) INTVALUE.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 2b279de39cf91c3919145735518034fc60cd3341
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917713"
---
# <a name="INTVALUE">De ER-functie INTVALUE</a>

[!include [banner](../includes/banner.md)]

De functie `INTVALUE` retourneert een *Int*-waarde voor de opgegeven tekenreeks.

## <a name="syntax-1"></a>Syntaxis 1

```
INTVALUE (text)
```

## <a name="syntax-2"></a>Syntaxis 2

```
INTVALUE (number)
```

## <a name="arguments"></a>Argumenten

`text`: *Tekenreeks*

Een tekstwaarde die moet worden geconverteerd naar een *Int*-getal.

`number`: *Werkelijk* of *Geheel getal*

Een numerieke waarde van het type *Werkelijk* of *Geheel getal* die moet worden geconverteerd naar een *Int*-getal.

## <a name="return-values"></a>Retourwaarden

*Int*

De resulterende numerieke waarde.

## <a name="usage-notes"></a>Gebruiksaanwijzingen

Eventuele cijfers achter de komma worden afgekapt.

## <a name="example-1"></a>Voorbeeld 1

`INTVALUE ("100.77")` retourneert de *Int*-waarde **100**.

## <a name="example-2"></a>Voorbeeld 2

`INTVALUE (-100.77)` retourneert de *Int*-waarde **-100**.

## <a name="additional-resources"></a>Aanvullende resources

[Type conversiefuncties](er-functions-category-type-conversion.md)
