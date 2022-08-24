---
title: De ER-functie DATEFORMAT
description: Dit artikel biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) DATEFORMAT.
author: kfend
ms.date: 09/08/2021
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
ms.openlocfilehash: 5a21e65df705e33c0bd502ea2c17e18b5385c0d4
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287393"
---
# <a name="dateformat-er-function"></a>De ER-functie DATEFORMAT

[!include [banner](../includes/banner.md)]

De functie `DATEFORMAT` retourneert een waarde van het type *[Tekenreeks](er-formula-supported-data-types-primitive.md#string)* voor een bepaalde datumwaarde als tekst in de opgegeven indeling en in een optioneel opgegeven [cultuur](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes). Zie voor informatie over de ondersteunde indelingen [standaard](/dotnet/standard/base-types/standard-date-and-time-format-strings) en [aangepast](/dotnet/standard/base-types/custom-date-and-time-format-strings).

## <a name="syntax-1"></a>Syntaxis 1

```vb
DATEFORMAT (date, format)
```

## <a name="syntax-2"></a>Syntaxis 2

```vb
DATEFORMAT (date, format, culture)
```

## <a name="arguments"></a>Argumenten

`date`: *[Datum](er-formula-supported-data-types-primitive.md#date)*

Een datumwaarde waarop de notatie moet worden toegepast.

`format`: *Tekenreeks*

De indeling van de uitvoertekenreeks. Zie voor informatie over de ondersteunde indelingen [standaard](/dotnet/standard/base-types/standard-date-and-time-format-strings) en [aangepast](/dotnet/standard/base-types/custom-date-and-time-format-strings).

> [!NOTE]
> De notatietekenreeks is hoofdlettergevoelig wanneer u een standaardnotatie of een aangepaste notatie gebruikt. De [standaard](/dotnet/standard/base-types/standard-date-and-time-format-strings) specificatie voor de notatie "d" bijvoorbeeld retourneert de datum met het patroon voor een korte datum, terwijl de standaard specificatie voor de notatie "D" de datum retourneert met het patroon voor de lange datum. Verder retourneert de [aangepaste](/dotnet/standard/base-types/custom-date-and-time-format-strings) specificatie voor de notatie "M" de maand van 1 t/m 12, terwijl de aangepaste specificatie voor de notatie "m" de minuut van 0 t/m 59 retourneert.

`culture`: *Tekenreeks*

De cultuur die moet worden gebruikt voor de indeling. Voor meer informatie over de ondersteunde culturen zie [cultuur](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).

## <a name="return-values"></a>Retourwaarden

*Tekenreeks*

De resulterende tekenreekswaarde.

## <a name="usage-notes"></a>Gebruiksaanwijzingen

Wanneer de cultuur niet is gedefinieerd als een argument van de aangeroepen functie, wordt de waarde van `culture` gedefinieerd door de aanroepcontext. Als de functie `DATEFORMAT` bijvoorbeeld wordt aangeroepen met syntaxis 1 in een ER-indeling (Elektronische rapportage) voor een element **FILE** dat is geconfigureerd voor gebruik van de Duitse cultuur, wordt de conversie uitgevoerd met de Duitse cultuur. De standaardwaarde van `culture` is **EN-US**.

## <a name="example-1"></a>Voorbeeld 1

`DATEFORMAT (TODAY (), "dd-MM-yyyy")` retourneert de datum/tijd van de huidige toepassingsserver, 24 december 2015, als de tekenreeks **24-12-2015**, op basis van de opgegeven aangepaste notatie.

## <a name="example-2"></a>Voorbeeld 2

`DATEFORMAT (SESSIONTODAY (), "d", "DE")` retourneert de huidige sessiedatum van de toepassing, 24 december 2015, als de tekenreeks **24-12-2015**, op basis van de geselecteerde Duitse cultuur en de opgegeven notatie.

## <a name="additional-resources"></a>Aanvullende resources

[Datum- en tijdfuncties](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
