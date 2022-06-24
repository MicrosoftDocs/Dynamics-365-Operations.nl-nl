---
title: De ER-functie REVERSE
description: Dit artikel biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) REVERSE.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: fce611b755865db15e8877e58d59bdf36bc730fe
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881514"
---
# <a name="reverse-er-function"></a>De ER-functie REVERSE

[!include [banner](../includes/banner.md)]

De functie `REVERSE` retourneert de opgegeven lijst als een *recordlijstwaarde* in omgekeerde sorteervolgorde.

## <a name="syntax"></a>Syntaxis

```vb
REVERSE (list)
```

## <a name="arguments"></a>Argumenten

`list`: *Recordlijst*

Het geldige pad van een gegevensbron van het gegevenstype *Recordlijst*.

## <a name="return-values"></a>Retourwaarden

*Recordlijst*

De resulterende lijst met records.

## <a name="example-1"></a>Voorbeeld 1

Als u de gegevensbron **DS** van het type *Berekend veld* invoert en deze de expressie `SPLIT ("C|B|A", "|")` bevat, retourneert de expressie `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` de tekstwaarde **C**.

## <a name="example-2"></a>Voorbeeld 2

Wanneer **Leverancier**  als een ER-gegevensbron (Elektronische rapportage) wordt geconfigureerd die naar de tabel VendTable verwijst, retourneert de expressie `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` een lijst met leveranciers die in aflopende volgorde op naam is gesorteerd.

## <a name="additional-resources"></a>Aanvullende resources

[Lijstfuncties](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]