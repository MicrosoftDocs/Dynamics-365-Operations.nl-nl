---
title: De ER-functie INDEX
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) INDEX.
author: NickSelin
ms.date: 05/20/2021
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
ms.openlocfilehash: 5a0fdb8958670efe8e2a37cee183bf836fa6c7e8
ms.sourcegitcommit: 047b0503868cc7d7b21868e24405d76af35db747
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/21/2021
ms.locfileid: "6087746"
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

> [!NOTE]
> Omdat nummering op basis van één wordt gebruikt voor deze functie, geeft u de waarde **1** op om de eerste record in de opgegeven lijst te retourneren.

## <a name="return-values"></a>Retourwaarden

*Container (record)*

De resulterende recordwaarde.

## <a name="example-1"></a>Voorbeeld 1

Als u de gegevensbron **DS** van het type *Berekend veld* invoert en deze de expressie `SPLIT ("A|B|C", "|")` bevat, retourneert de expressie `DS.Value` de tekstwaarde **B** voor de tweede record van deze recordlijst. De expressie `INDEX (SPLIT ("A|B|C", "|"), 2).Value` retourneert ook de tekstwaarde **B**.

## <a name="example-2"></a>Voorbeeld 2

Als u de gegevensbron **DS** van het type *Berekend veld* invoert en deze de expressie `SPLIT ("A|B|C", "|")` bevat, genereert de expressie `INDEX (SPLIT ("A|B|C", "|"), 4).Value` een uitzondering tijdens runtime.

## <a name="additional-resources"></a>Aanvullende resources

[Lijstfuncties](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
