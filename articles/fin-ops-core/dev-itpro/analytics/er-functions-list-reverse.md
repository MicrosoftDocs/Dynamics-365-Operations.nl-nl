---
title: De ER-functie REVERSE
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) REVERSE.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 746a736c8797c1c1c5bd71d7d803be4212984595
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755199"
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