---
title: De ER-functie ADDDAYS
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) ADDDAYS.
author: NickSelin
manager: kfend
ms.date: 12/03/2019
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
ms.openlocfilehash: 08b9727fb34210fecff31826cc1f2b8da022156b
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042453"
---
# <a name="ADDDAYS">De ER-functie ADDDAYS</a>

[!include [banner](../includes/banner.md)]

De functie `ADDDAYS` berekent een waarde van het type *DateTime* voor het opgegeven aantal dagen vóór of na een opgegeven begindatum.

## <a name="syntax"></a>Syntaxis

```vb
ADDDAYS (datetime, days)
```

## <a name="arguments"></a>Argumenten

`datetime`: *DateTime*

Een datum-/tijdwaarde voor de begindatum.

`days`: *Geheel getal*

Het aantal dagen voor of na `datetime`.

## <a name="return-values"></a>Retourwaarden

*Datum/tijd*

De resulterende datum-/tijdwaarde.

## <a name="usage-notes"></a>Gebruiksaanwijzingen

Een positieve waarde voor `days` levert een toekomstige datum op. Een negatieve waarde resulteert in een datum in het verleden.

## <a name="example-1"></a>Voorbeeld 1

`ADDDAYS (NOW(), 7)` retourneert de datum en tijd over zeven dagen.

## <a name="example-2"></a>Voorbeeld 2

`ADDDAYS (NOW(), -3)` retourneert de datum en tijd van drie dagen geleden.

## <a name="additional-resources"></a>Aanvullende resources

[Datum- en tijdfuncties](er-functions-category-datetime.md)
