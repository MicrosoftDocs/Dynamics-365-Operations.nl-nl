---
title: ER-functie EMPTYRECORD
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) EMPTYRECORD.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 2d3c34cbff8551b84121201b9489250c07c7799e
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563241"
---
# <a name="emptyrecord-er-function"></a>ER-functie EMPTYRECORD

[!include [banner](../includes/banner.md)]

De functie `EMPTYRECORD` retourneert een nulwaarde voor *Container (record)* met dezelfde structuur als de opgegeven recordlijst of record.

## <a name="syntax"></a>Syntaxis

```vb
EMPTYRECORD (list)
```

## <a name="arguments"></a>Argumenten

`list`: *Recordlijst* of *Container (record)*

Het geldige pad van een gegevensbron van het type *Recordlijst* of *Container (record)*.

## <a name="return-values"></a>Retourwaarden

*Container (record)*

De resulterende recordwaarde.

## <a name="usage-notes"></a>Gebruiksaanwijzingen

> [!NOTE] 
> Een null-record is een record waarin alle velden een lege waarde hebben. Een lege waarde is **0** (nul) voor getallen, een lege tekenreeks voor tekenreeksen, enzovoort.

## <a name="example"></a>Voorbeeld

`EMPTYRECORD (SPLIT ("abc", 1))` retourneert een nieuwe lege record die dezelfde structuur heeft als de lijst die wordt geretourneerd door de functie `SPLIT`. Zie voor meer informatie [SPLIT](er-functions-list-split.md).

## <a name="additional-resources"></a>Aanvullende resources

[Registratiefuncties](er-functions-category-record.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]