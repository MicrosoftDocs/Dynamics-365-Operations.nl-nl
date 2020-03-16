---
title: De ER-functie JSONVALUE
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) JSONVALUE.
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 75f20632074cb4dead98991fd6522ab9b20b9965
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041211"
---
# <a name="JSONVALUE">De ER-functie JSONVALUE</a>

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
