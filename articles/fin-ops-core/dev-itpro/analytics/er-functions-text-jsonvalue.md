---
title: De ER-functie JSONVALUE
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) JSONVALUE.
author: NickSelin
ms.date: 12/11/2019
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
ms.openlocfilehash: e8336e43a236e3f3b875fb3cb81bc139507673c2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746358"
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

De id van een scalaire waarde van JSON-gegevens.

## <a name="return-values"></a>Retourwaarden

*Tekenreeks*

De resulterende tekstwaarde.

## <a name="example"></a>Voorbeeld

De gegevensbron **JsonField** bevat de volgende gegevens in JSON-indeling: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**. In dit geval retourneert de expressie `JSONVALUE (JsonField, "BuildNumber")` de volgende waarde van het gegevenstype *Tekenreeks*: **7.3.1234.1.**

## <a name="additional-resources"></a>Aanvullende resources

[Tekstfuncties](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]