---
title: De ER-functie DATEVALUE
description: Dit artikel biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) DATEVALUE.
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
ms.openlocfilehash: 290a4665d3527c0f0954c46cb0a0a14677b93218
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268693"
---
# <a name="datevalue-er-function"></a>De ER-functie DATEVALUE

[!include [banner](../includes/banner.md)]

De functie `DATEVALUE` retourneert een *[datumwaarde](er-formula-supported-data-types-primitive.md#date)* die van een bepaalde tekstwaarde in de opgegeven indeling en in een optioneel opgegeven [cultuur](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) wordt geconverteerd naar een datumwaarde. Zie voor informatie over de ondersteunde indelingen [standaard](/dotnet/standard/base-types/standard-date-and-time-format-strings) en [aangepast](/dotnet/standard/base-types/custom-date-and-time-format-strings).

## <a name="syntax-1"></a>Syntaxis 1

```vb
DATEVALUE (text, format)
```

## <a name="syntax-2"></a>Syntaxis 2

```vb
DATEVALUE (text, format, culture)
```

## <a name="arguments"></a>Argumenten

`text`: *[Tekenreeks](er-formula-supported-data-types-primitive.md#string)*

Tekst die de in te delen waarde vertegenwoordigt.

`format`: *Tekenreeks*

De indeling van de betreffende tekst. Zie voor informatie over de ondersteunde indelingen [standaard](/dotnet/standard/base-types/standard-date-and-time-format-strings) en [aangepast](/dotnet/standard/base-types/custom-date-and-time-format-strings).

`culture`: *Tekenreeks*

De cultuur die wordt gebruikt voor het indelen van de betreffende tekst. Voor meer informatie over de ondersteunde culturen zie [cultuur](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).

## <a name="return-values"></a>Retourwaarden

*Datum*

De resulterende datumwaarde.

## <a name="usage-notes"></a>Gebruiksaanwijzingen

Wanneer de cultuur niet is gedefinieerd als een argument van de aangeroepen functie, wordt de waarde van `culture` gedefinieerd door de aanroepcontext. Als de functie `DATEVALUE` bijvoorbeeld wordt aangeroepen met syntaxis 1 in een ER-indeling (Elektronische rapportage) voor een element **FILE** dat is geconfigureerd voor gebruik van de Duitse cultuur, wordt de conversie uitgevoerd met de Duitse cultuur. De standaardwaarde van `culture` is **EN-US**.

## <a name="example-1"></a>Voorbeeld 1

`DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")` retourneert de datumwaarde **21 december 2016** volgens de opgegeven aangepaste notatie en de cultuur **EN-US** van de standaardtoepassing.

## <a name="example-2"></a>Voorbeeld 2

`DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")` retourneert de datumwaarde **21 januari 2016**, gebaseerd op de opgegeven aangepaste indeling en cultuur.

Echter, `DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")` leidt tot een uitzondering en informeert de gebruiker dat de opgegeven tekenreeks niet als een geldige datum wordt herkend voor de opgegeven cultuur.

## <a name="additional-resources"></a>Aanvullende resources

[Datum- en tijdfuncties](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
