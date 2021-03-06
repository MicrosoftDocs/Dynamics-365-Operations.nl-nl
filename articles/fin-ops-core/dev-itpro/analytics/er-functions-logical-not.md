---
title: De ER-functie NOT
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) NOT.
author: NickSelin
ms.date: 12/17/2019
ms.topic: article
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
ms.openlocfilehash: 7c10ed61b97dcd4d4a66a530bb3d08c539659233
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751702"
---
# <a name="not-er-function"></a>De ER-functie NOT

[!include [banner](../includes/banner.md)]

De functie `NOT` retourneert de omgekeerde logische waarde van de opgegeven voorwaarde als een *Booleaanse* waarde.

## <a name="syntax"></a>Syntaxis

```vb
NOT (condition)
```

## <a name="arguments"></a>Argumenten

`condition`: *Booleaans*

Een geldige voorwaardelijke expressie die moet worden omgekeerd.

## <a name="return-values"></a>Retourwaarden

*Booleaans*

De resulterende *Booleaanse* waarde.

## <a name="example"></a>Voorbeeld

`NOT (TRUE)` retourneert **FALSE**.

## <a name="additional-resources"></a>Aanvullende resources

[Logische functies](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]