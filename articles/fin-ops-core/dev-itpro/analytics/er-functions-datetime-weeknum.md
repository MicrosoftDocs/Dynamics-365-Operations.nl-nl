---
title: De ER-functie WEEKNUM
description: Dit artikel biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) WEEKNUM.
author: kfend
ms.date: 01/15/2022
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-12-03
ms.dyn365.ops.version: AX 10.0.24
ms.custom: 58771
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 4658f88b7e353e651177fad0c8636c5403be1256
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268141"
---
# <a name="weeknum-er-function"></a>De ER-functie WEEKNUM

[!include [banner](../includes/banner.md)]

De functie `WEEKNUM` retourneert een *[geheel getal](er-formula-supported-data-types-primitive.md#integer)* dat staat voor de week van het jaar met een opgegeven *[datum](er-formula-supported-data-types-primitive.md#date)*. De berekening is gebaseerd op cultuurafhankelijke regels die een kalenderweek en de eerste dag van de week definiëren.

## <a name="syntax"></a>Syntaxis

```vb
WEEKNUM (date, culture) as Integer
```

## <a name=""></a><a name="arguments">Argumenten</a>

`date`: *Datum*

Een datumwaarde die de datum voor de berekening van de week van het jaar vertegenwoordigt.

`culture`: *[Tekenreeks](er-formula-supported-data-types-primitive.md#string)*

De cultuur die moet worden gebruikt voor de berekening. U kunt cultuurcodes gebruiken die worden ondersteund in overeenstemming met .NET-[standaarden](/dotnet/api/system.globalization.cultureinfo.getcultures?view=net-5.0).

## <a name="return-values"></a>Retourwaarden

*Geheel getal*

De resulterende numerieke waarde.

## <a name="usage-notes"></a>Gebruiksaanwijzingen

De week van het jaar wordt berekend op basis van de [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html)-standaard, als deze standaard is aangenomen door een land of regio waar de landinstelling voor is opgegeven tijdens runtime. Anders wordt de berekening gebaseerd op land-/regiospecifieke nationale standaarden.

Als een niet-ondersteunde [cultuur](#arguments)code wordt geleverd als argument van de functie `WEEKNUM` tijdens runtime, treedt een uitzondering op. Als de lege tekenreeks wordt opgegeven als een cultuurcode, wordt de Engelse landneutrale kalender gebruikt om het weeknummer te berekenen.

## <a name="examples"></a>Voorbeelden

`WEEKNUM (DATEVALUE ("01-01-2020", "de"))` retourneert **1**.

`WEEKNUM (DATEVALUE ("01-01-2021", "de"))` retourneert **53**.

`WEEKNUM (DATEVALUE ("01-01-2022", "de"))` retourneert **52**.

`WEEKNUM (DATEVALUE ("01-01-2022", "ar"))` retourneert **21**.

## <a name="additional-resources"></a>Aanvullende bronnen

[Datum- en tijdfuncties](er-functions-category-datetime.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
