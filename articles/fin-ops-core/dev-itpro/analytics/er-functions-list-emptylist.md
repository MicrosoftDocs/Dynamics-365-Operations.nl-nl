---
title: De ER-functie EMPTYLIST
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) EMPTYLIST.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: ccb52d7d88f292720360ae913ead5be239165193
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687665"
---
# <a name="emptylist-er-function"></a>De ER-functie EMPTYLIST

[!include [banner](../includes/banner.md)]

De functie `EMPTYLIST` retourneert een lege waarde van het type *Recordlijst* door de opgegeven lijst te gebruiken als een bron voor de lijststructuur.

## <a name="syntax"></a>Syntaxis

```vb
EMPTYLIST (list)
```

## <a name="arguments"></a>Argumenten

`list`: *Recordlijst*

Het geldige pad van een gegevensbron van het gegevenstype *Recordlijst*.

## <a name="return-values"></a>Retourwaarden

*Recordlijst*

De resulterende lijst met records.

## <a name="example"></a>Voorbeeld

`EMPTYLIST (SPLIT ("abc", 1))` retourneert een nieuwe lege lijst die dezelfde structuur heeft als de lijst die wordt geretourneerd door de gebruikte functie `SPLIT`.

## <a name="additional-resources"></a>Aanvullende resources

[Lijstfuncties](er-functions-category-list.md)
