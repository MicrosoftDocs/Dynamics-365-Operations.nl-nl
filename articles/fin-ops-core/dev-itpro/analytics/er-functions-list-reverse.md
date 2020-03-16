---
title: De ER-functie REVERSE
description: Dit onderwerp biedt informatie over het gebruik van de ER-functie (Elektronische rapportage) REVERSE.
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
ms.openlocfilehash: a6134ae7eb1a8044cf906f2a8d02eb153522a6cf
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041924"
---
# <a name="REVERSE">De ER-functie REVERSE</a>

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
