---
title: De ER-functie INDEX
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) INDEX.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 051e22daa3fe2d6c328e36403201d940f724bd29
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745172"
---
# <a name="index-er-function"></a>De ER-functie INDEX

[!include [banner](../includes/banner.md)]

De functie `INDEX` retourneert een waarde van het type *Container (record)* die wordt geselecteerd op basis van de opgegeven numerieke index in de opgegeven lijst. Er wordt een uitzondering gegenereerd als de index zich buiten het bereik van de records in de opgegeven lijst bevindt.

## <a name="syntax"></a>Syntaxis

```vb
INDEX (list, index)
```

## <a name="arguments"></a>Argumenten

`list`: *Recordlijst*

Het geldige pad van een gegevensbron van het gegevenstype *Recordlijst*.

`index`: *Geheel getal*

Een numerieke index die de positie van de gewenste record in de opgegeven lijst aangeeft.

## <a name="return-values"></a>Retourwaarden

*Container (record)*

De resulterende recordwaarde.

## <a name="example-1"></a>Voorbeeld 1

Als u de gegevensbron **DS** van het type *Berekend veld* invoert en deze de expressie `SPLIT ("A|B|C", "|")` bevat, retourneert de expressie `DS.Value` de tekstwaarde **B** voor de tweede record van deze recordlijst. De expressie `INDEX (SPLIT ("A|B|C", "|"), 2).Value` retourneert ook de tekstwaarde **B**.

## <a name="example-2"></a>Voorbeeld 2

Als u de gegevensbron **DS** van het type *Berekend veld* invoert en deze de expressie `SPLIT ("A|B|C", "|")` bevat, genereert de expressie `INDEX (SPLIT ("A|B|C", "|"), 4).Value` een uitzondering tijdens runtime.

## <a name="additional-resources"></a>Aanvullende resources

[Lijstfuncties](er-functions-category-list.md)
