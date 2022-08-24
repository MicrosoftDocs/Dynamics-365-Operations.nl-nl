---
title: De ER-functie TRIM
description: Dit artikel biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) TRIM.
author: kfend
ms.date: 02/28/2022
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
ms.openlocfilehash: 95b8d2989d705c4998da0af8e683adf567edfe92
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273093"
---
# <a name="trim-er-function"></a>De ER-functie TRIM

[!include [banner](../includes/banner.md)]

De functie `TRIM` retourneert de opgegeven tekenreeks als *tekenreekswaarde* nadat tekens voor tabblad, regelterugloop, regeldoorvoer en formulierfeed zijn vervangen door één spatieteken, nadat voor- en navolgende spaties zijn ingekort en nadat meerdere spaties tussen woorden zijn verwijderd.

## <a name="syntax"></a>Syntaxis

```vb
TRIM (text)
```

## <a name="arguments"></a>Argumenten

`text`: *Tekenreeks*

Het geldige pad van een gegevensbron van het type *Tekenreeks*.

## <a name="return-values"></a>Retourwaarden

*Tekenreeks*

De resulterende tekstwaarde.

## <a name="usage-notes"></a>Gebruiksaanwijzingen

In sommige gevallen wilt u voor- en navolgende spaties afkappen, maar de voorkeur is het behouden van opmaak voor de opgegeven tekst. Bijvoorbeeld: wanneer deze tekst een adres vertegenwoordigt dat kan worden ingevoerd in het tekstvak met meerdere regels met teruglopen en nieuwe regels. Gebruik in dit geval de volgende expressie: `REPLACE(text,"^[ \t]+|[ \t]+$","", true)` waar `text` het argument is dat naar de opgegeven tekstreeks verwijst.

## <a name="example-1"></a>Voorbeeld 1

`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` retourneert **Sample text**.

## <a name="example-2"></a>Voorbeeld 2

`TRIM (CONCATENATE (CHAR(10), "`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`", CHAR(9),"`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`", CHAR(13)))` geeft **"Voorbeeldtekst"**.

## <a name="additional-resources"></a>Aanvullende bronnen

[Tekstfuncties](er-functions-category-text.md)

[De ER-functie REPLACE](er-functions-text-replace.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
