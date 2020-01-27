---
title: De ER-functie NULLCONTAINER
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) NULLCONTAINER.
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
ms.openlocfilehash: 1dde102acf18e451cb895b51b28d22102f38936c
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915781"
---
# <a name="NULLCONTAINER">De ER-functie NULLCONTAINER</a>

[!include [banner](../includes/banner.md)]

De functie `NULLCONTAINER` retourneert een nulwaarde voor *Container (record)* met dezelfde structuur als de opgegeven recordlijst of record.

## <a name="syntax"></a>Syntaxis

```
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
