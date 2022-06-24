---
title: De ER-functie JSONVALUE
description: Dit artikel biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) JSONVALUE.
author: NickSelin
ms.date: 10/25/2021
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
ms.openlocfilehash: 7deaed83959f033d11333efb5a2b398cbe57076d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909495"
---
# <a name="jsonvalue-er-function"></a>De ER-functie JSONVALUE

[!include [banner](../includes/banner.md)]

De functie `JSONVALUE` parseert gegevens in de indeling JavaScript Object Notation (JSON), die kan worden geopend op het opgegeven pad, en er wordt een scalaire waarde met de opgegeven id geëxtraheerd. Vervolgens wordt de geëxtraheerde scalaire waarde als een *tekenreekswaarde* geretourneerd.

## <a name="syntax"></a>Syntaxis

```vb
JSONVALUE (input, path)
```

## <a name="arguments"></a>Argumenten

`input`: *Tekenreeks*

Het geldige pad van een gegevensbron van het type *Tekenreeks* die JSON-gegevens bevat.

`path`: *Tekenreeks*

De id van een scalaire waarde van JSON-gegevens. Gebruik een slash (/) om de namen van gerelateerde JSON-knooppunten te scheiden. Gebruik de notatie met haakjes (\[\]) om de index van een bepaalde waarde in een JSON-matrix op te geven. Voor deze index wordt gebruik gemaakt van nummering op basis van nul.

## <a name="return-values"></a>Retourwaarden

*Tekenreeks*

De resulterende tekstwaarde.

## <a name="example-1"></a>Voorbeeld 1

De gegevensbron **JsonField** bevat de volgende gegevens in JSON-indeling: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**. In dit geval retourneert de expressie `JSONVALUE (JsonField, "BuildNumber")` de volgende waarde van het gegevenstype *Tekenreeks*: **7.3.1234.1.**

## <a name="example-2"></a>Voorbeeld 2

De gegevensbron **JsonField** van het type *Berekend veld* bevat de volgende expressie: `"{""workers"": [ {""name"": ""Adam"", ""age"": 30, ""emails"": [""AdamS@Contoso.com"", ""AdamS@Hotmail.com"" ]}, { ""name"": ""John"", ""age"": 21, ""emails"": [""JohnS@Contoso.com"", ""JohnS@Aol.com""]}]}"`.

Deze expressie die is geconfigureerd om een waarde van het type [*Tekenreeks*](er-formula-supported-data-types-primitive.md#string) te retourneren vertegenwoordigt de volgende gegevens in de JSON-indeling.

```json
{
    "workers": [
        {
            "name": "Adam",
            "age": 30,
            "emails": [ "AdamS@Contoso.com", "AdamS@Hotmail.com" ]
        },
        {
            "name": "John",
            "age": 21,
            "emails": [ "JohnS@Contoso.com", "JohnS@Aol.com" ]
        }
    ]
}
```

In dit geval retourneert de expressie `JSONVALUE(json, "workers/[1]/emails/[0]")` de volgende waarde van het gegevenstype *Tekenreeks*: `JohnS@Contoso.com`.

## <a name="additional-resources"></a>Aanvullende bronnen

[Tekstfuncties](er-functions-category-text.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
