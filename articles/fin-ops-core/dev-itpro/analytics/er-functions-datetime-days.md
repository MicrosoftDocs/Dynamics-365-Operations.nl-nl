---
title: De ER-functie DAYS
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) DAYS.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 4f8c12a22f7654285d5598064473bf86689ed207
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916287"
---
# <a name="DAYS">De ER-functie DAYS</a>

[!include [banner](../includes/banner.md)]

De functie `DAYS` retourneert een *geheel getal* dat staat voor het aantal dagen tussen de ene en een andere opgegeven datum.

## <a name="syntax"></a>Syntaxis

```
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
