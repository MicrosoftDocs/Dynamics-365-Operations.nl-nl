---
title: De ER-functie NULLCONTAINER
description: Dit artikel biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) NULLCONTAINER.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 8da2a30cf2839adabf7b5ea4916f44999aa05758
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850953"
---
# <a name="nullcontainer-er-function"></a>De ER-functie NULLCONTAINER

[!include [banner](../includes/banner.md)]

De functie `NULLCONTAINER` retourneert een nulwaarde voor *Container (record)* met dezelfde structuur als de opgegeven recordlijst of record.

## <a name="syntax"></a>Syntaxis

```vb
NULLCONTAINER (list)
```

## <a name="arguments"></a>Argumenten

`list`: *Recordlijst* of *Container (record)*

Het geldige pad van een gegevensbron van het type *Recordlijst* of *Container (record)*.

## <a name="return-values"></a>Retourwaarden

*Container (record)*

De resulterende recordwaarde.

## <a name="usage-notes"></a>Gebruiksaanwijzingen

> [!NOTE] 
> Deze functie is verouderd. Gebruik in plaats daarvan de functie `EMPTYRECORD`. Zie voor meer informatie [EMPTYRECORD](er-functions-record-emptyrecord.md).

## <a name="example"></a>Voorbeeld

`NULLCONTAINER (SPLIT ("abc", 1))` retourneert een nieuwe lege record die dezelfde structuur heeft als de lijst die wordt geretourneerd door de functie `SPLIT`. Zie voor meer informatie [SPLIT](er-functions-list-split.md).

## <a name="additional-resources"></a>Aanvullende resources

[Registratiefuncties](er-functions-category-record.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]