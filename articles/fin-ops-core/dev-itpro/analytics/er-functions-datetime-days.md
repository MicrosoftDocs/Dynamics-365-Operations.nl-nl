---
title: De ER-functie DAYS
description: Dit artikel biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) DAYS.
author: kfend
ms.date: 12/04/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: a0c50e36bbf0c2bd999a17631e3e00d2feb162fd
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268720"
---
# <a name="days-er-function"></a>De ER-functie DAYS

[!include [banner](../includes/banner.md)]

De functie `DAYS` retourneert een *geheel getal* dat staat voor het aantal dagen tussen de ene en een andere opgegeven datum.

## <a name="syntax"></a>Syntaxis

```vb
DAYS (date 1, date 2) as Integer
```

## <a name="arguments"></a>Argumenten

`date 1`: *Datum*

Een datumwaarde die de begindatum voor de berekening van het aantal dagen vertegenwoordigt.

`date 2`: *Datum*

Een datumwaarde die de einddatum voor de berekening van het aantal dagen vertegenwoordigt.

## <a name="return-values"></a>Retourwaarden

*Geheel getal*

De resulterende numerieke waarde.

## <a name="usage-notes"></a>Gebruiksaanwijzingen

De functie `DAYS` retourneert een positieve waarde wanneer de eerste datum later is dan de tweede datum, **0** (nul) als de eerste datum gelijk is aan de tweede datum en een negatieve waarde als de eerste datum vroeger is dan de tweede datum.

## <a name="example"></a>Voorbeeld

`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` retourneert **-1**.

## <a name="additional-resources"></a>Aanvullende resources

[Datum- en tijdfuncties](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
