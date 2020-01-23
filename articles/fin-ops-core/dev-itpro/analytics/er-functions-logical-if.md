---
title: De ER-functie IF
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) IF.
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
ms.openlocfilehash: b29302ffe534f2439519e57c6a6b8c94c1df8d62
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917138"
---
# <a name="IF">De ER-functie IF</a>

[!include [banner](../includes/banner.md)]

De functie `IF` retourneert de eerste opgegeven waarde als aan de opgegeven voorwaarde is voldaan. Anders wordt de tweede opgegeven waarde als resultaat gegeven. De geretourneerde waarde kan een waarde zijn van een van de ondersteunde gegevenstypen.

## <a name="syntax"></a>Syntaxis

```
IF (condition, first value, second value) as any of the supported data types
```

## <a name="arguments"></a>Argumenten

`condition`: *Booleaans*

Een geldige voorwaardelijke expressie die moet worden getest.

`first value`: *Een van de ondersteunde gegevenstypen*

Het resultaat dat wordt geretourneerd als aan de voorwaarde wordt voldaan.

`second value`: *Een van de ondersteunde gegevenstypen*

Het resultaat dat wordt geretourneerd als niet aan de voorwaarde wordt voldaan.

## <a name="return-values"></a>Retourwaarden

*Een van de ondersteunde gegevenstypen*

De resulterende waarde van een van de ondersteunde gegevenstypen.

## <a name="usage-notes"></a>Gebruiksaanwijzingen

De argumenten `first value` en `second value` moeten worden opgegeven met hetzelfde gegevenstype. Er wordt een uitzondering gegenereerd tijdens het ontwerpen als de gegevenstypen van de geconfigureerde waarden niet overeenkomen.

Als de eerste en tweede waarden van het gegevenstype *Container (record)* of *Recordlijst* zijn, bevat het resultaat alleen de velden die in beide waarden bestaan.

## <a name="example"></a>Voorbeeld

`IF (1=2, "condition is met", "condition is not met")` retourneert de tekenreeks **"condition is not met"**.

## <a name="additional-resources"></a>Aanvullende resources

[Logische functies](er-functions-category-logical.md)
