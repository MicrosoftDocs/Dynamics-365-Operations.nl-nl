---
title: De ER-functie AND
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) AND.
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dd9c0ed0238009f70ad7a9bf5a5e19ebfb95cccc
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917161"
---
# <a name="AND">De ER-functie AND</a>

[!include [banner](../includes/banner.md)]

De functie `AND` retourneert de *Booleaanse waarde* **TRUE** als alle opgegeven voorwaarden waar zijn. Anders wordt de *Booleaanse* waarde **FALSE** geretourneerd.

## <a name="syntax"></a>Syntaxis

```
AND (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a>Argumenten

`condition 1`: *Booleaans*

Een geldige voorwaardelijke expressie die moet worden getest. Dit argument is verplicht.

`condition N`: *Booleaans*

Een geldige voorwaardelijke expressie die moet worden getest. Deze aanvullende argumenten zijn optioneel.

## <a name="return-values"></a>Retourwaarden

*Booleaans*

De resulterende *Booleaanse* waarde.

## <a name="usage-notes"></a>Gebruiksaanwijzingen

In de argumenten van logische functies kunt u gegevensbronverwijzingen, numerieke en tekstwaarden, Booleaanse waarden, vergelijkingsoperatoren en andere ER-functies (Elektronische rapportage) gebruiken. Alle argumenten moeten echter worden geëvalueerd tot een *Booleaanse* waarde **TRUE** of **FALSE**.

## <a name="example"></a>Voorbeeld

`AND (1=1, "a"="a")` retourneert **TRUE**.

`AND (1=2, "a"="a")` retourneert **FALSE**.

## <a name="additional-resources"></a>Aanvullende resources

[Logische functies](er-functions-category-logical.md)
